<template>
  <div id="carouselExampleIndicators" class="carousel slide">
    <div class="carousel-indicators">
      <button
        v-for="(image, index) in images"
        :key="image.id"
        type="button"
        data-bs-target="#carouselExampleIndicators"
        :data-bs-slide-to="index"
        :class="{ active: index === 0 }"
        :aria-label="'Slide ' + (index + 1)"
      ></button>
    </div>

    <div class="carousel-inner">
      <div
        v-for="(image, index) in images"
        :key="image.id"
        :class="['carousel-item', { active: index === 0 }]"
      >
        <img :src="image.path_thumb" alt="Property Image" />
      </div>
    </div>

    <button
      class="carousel-control-prev"
      type="button"
      data-bs-target="#carouselExampleIndicators"
      data-bs-slide="prev"
    >
      <span class="carousel-control-prev-icon" aria-hidden="true"></span>
      <span class="visually-hidden">Previous</span>
    </button>

    <button
      class="carousel-control-next"
      type="button"
      data-bs-target="#carouselExampleIndicators"
      data-bs-slide="next"
    >
      <span class="carousel-control-next-icon" aria-hidden="true"></span>
      <span class="visually-hidden">Next</span>
    </button>
  </div>
</template>

<script setup>
defineProps(["images"]);
</script>

<style scoped>
.carousel {
  width: 100%;
}

img {
  width: 100%;
  object-fit: cover;
}
</style>
  