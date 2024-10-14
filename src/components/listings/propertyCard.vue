<template>
  <div class="property-card">
    <propertyImageSlider :images="property.images" />

    <div class="property-details">
      <div class="price-row">
        <p class="price">
          {{ property.currency ? property.currency : "N/A" }}
          {{ property.price ? property.price : "N/A" }}
        </p>
        <img src="../../assets/favourite.png" alt="" />
      </div>

      <p class="status">
        {{ property.status ? property.status : "N/A" }} |
        {{ property.type ? property.type : "N/A" }}
      </p>

      <h2 class="title">
        {{ property.property.name ? property.property.name : "N/A" }}
      </h2>
      <p class="description">
        {{ property.description ? property.description : "N/A" }}
      </p>

      <div class="location">
        <p class="address">
          {{ property.property.address ? property.property.address : "N/A" }}
        </p>
        <p class="distance">
          <img src="../../assets/location.png" alt="" />
          {{ property.property.distance ? property.property.distance : "N/A" }} KM
        </p>
      </div>

      <div class="facilities">
        <div class="facility">
          <img src="../../assets/bedrooms.png" alt="" />
          <p>
            {{ property.property.bedroom_nos ? property.property.bedroom_nos : "N/A" }}
          </p>
        </div>
        <div class="facility">
          <img src="../../assets/baths.png" alt="" />
          <p>
            {{ property.property.bathroom_nos ? property.property.bathroom_nos : "N/A" }}
          </p>
        </div>
        <div class="facility">
          <img src="../../assets/parking.png" alt="" />
          <p>
            {{ property.property.parking_nos ? property.property.parking_nos : "N/A" }}
          </p>
        </div>
        <div class="facility">
          <img src="../../assets/size.png" alt="" />
          <p>
            {{ property.property.size ? property.size : "N/A" }} {{ property.property.size_unit }}
          </p>
        </div>
      </div>

      <div class="author-info">
        <div class="d-flex w-100">
          <img
            :src="
              property.author.avatar
                ? property.author.avatar
                : 'default-avatar.png'
            "
            alt="author Image"
            class="author-avatar"
          />
          <div class="author-details">
            <p class="author-name">
              {{ property.author.name ? property.author.name : "N/A" }}
            </p>
            <p class="author-company">
              {{ property.author.company ? property.author.company : "N/A" }}
            </p>
          </div>
        </div>

        <div class="contact-info">
          <p class="w-100 contact-number">
            <i class="phone-icon">📞</i>
            {{ property.author.phone ? property.author.phone : "N/A" }}
          </p>
          <div class="contact-icons d-flex">
            <img style="width: 70px" src="../../assets/contact.png" alt="" />
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script setup>
defineProps(["property"]);
import propertyImageSlider from "./propertyImageSlider.vue";
</script>

<style scoped>
.property-card {
  display: flex;
  overflow: hidden;
  padding: 5px;
  border-bottom: 2px solid #dbdbdb;
}
p {
  font-size: 12px;
  margin-bottom: 10px !important;
}
img {
  width: 20px;
}

.property-image-slider {
  width: 100%;
  height: 220px;
  object-fit: cover;
}

.property-details {
  padding: 5px;
  width: 100%;
}

.price-row {
  display: flex;
  justify-content: space-between;
  align-items: baseline;
  height: 30px;
}

.price {
  font-weight: bold;
  font-size: 12px;
  color: #333;
}

.heart-icon {
  font-size: 20px;
  color: #999;
  cursor: pointer;
}

.status {
  font-size: 12px;
  color: #666;
}

.title {
  font-size: 12px;
  margin: 0.5rem 0;
  font-weight: bold;
}

.description {
  color: #777;
  /* margin-bottom: 1rem; */
  font-size: 12px;
}

.location {
  display: flex;
  justify-content: space-between;
  /* margin-bottom: 1rem; */
  color: #555;
}

.facilities {
  display: flex;
  justify-content: space-around;
  color: #555;
}

.facility {
  display: flex;
  align-items: center;
  gap: 5px;
}

.facility p {
  margin: 0px !important;
}

.author-info {
  display: flex;
  flex-direction: column;
  align-items: flex-start;
  /* border-top: 1px solid #e0e0e0; */
  margin-top: 1.5rem;
}

.author-avatar {
  width: 48px;
  height: 48px;
  border-radius: 50%;
  margin-right: 1rem;
}

.author-details {
  flex-grow: 1;
}

.contact-info {
  display: flex;
  justify-content: space-between;
  align-items: center;
  /* gap: 10px; */
  width: 100%;
}
.contact-number {
  background-color: #dbdbdb;
  height: 28px;
  padding: 5px;
  margin: 0px !important;
}
.contact-icons i {
  font-size: 18px;
  cursor: pointer;
}
</style>
