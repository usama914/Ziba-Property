<template>
  <div class="author-card">
    <div class="d-flex">
      <img :src="author.avatar" alt="Author Image" class="author-avatar" />
      <div class="author-details">
        <h3 class="author-name">{{ author.name }}</h3>
        <p class="author-company">{{ author.company }}</p>
        <p class="author-listings">{{ author.listings }} Listings</p>
      </div>
    </div>
    <div class="contact-info">
      <p class="w-100 contact-number">
        <i class="phone-icon">📞</i>
        {{ author.phone ? author.phone : "N/A" }}
      </p>
      <div class="contact-icons d-flex">
        <img style="width: 60px" src="../../assets/contact.png" alt="" />
      </div>
    </div>
  </div>
</template>

<script setup>
defineProps(["author"]);
</script>

<style scoped>
.author-card {
  display: flex;
  flex-direction: column;
  align-items: flex-start;
  padding: 5px;
  background-color: #fff;
  font-family: "Arial", sans-serif;
  border-top: 1px solid #ddd;
  border-bottom: 1px solid #ddd;
}

.author-card:first-child {
  border-radius: 12px 12px 0 0;
}

.author-card:last-child {
  border-radius: 0 0 12px 12px;
}

.author-avatar {
  width: 60px;
  height: 60px;
  border-radius: 50%;
  object-fit: cover;
  margin-right: 1rem;
}

.author-details {
  flex-grow: 1;
}

.author-name {
  font-size: 18px;
  font-weight: bold;
  margin: 0;
  color: #6d6dd8;
}

.author-company {
  font-size: 14px;
  color: #666;
}

.author-listings {
  font-size: 14px;
  color: #333;
}

.contact-info {
  display: flex;
  justify-content: space-between;
  align-items: center;
  /* gap: 10px; */
  width: 100%;
}
.contact-info p{
font-size: 10px;
}
.contact-number {
  background-color: #dbdbdb;
  height: 23px;
  padding: 5px;
  margin: 0px !important;
}

.phone-section {
  display: flex;
  align-items: baseline;
  gap: 5px;
}

.phone-number {
  font-size: 14px;
  color: #333;
}

.contact-icons {
  display: flex;
  gap: 8px;
}

.whatsapp-button,
.email-button {
  border: none;
  background: none;
  cursor: pointer;
  font-size: 20px;
}

.whatsapp-icon {
  color: green;
}

.email-icon {
  color: #555;
}
</style>
