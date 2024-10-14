<template>
  <div class="home">
    <propertyListing></propertyListing>
  </div>
</template>
<script setup>
import propertyListing from "../pages/propertyListing.vue";
</script>
<style>
@media (min-width: 1024px) {
  .home {
    min-height: 100vh;
    /* display: flex; */
    /* align-items: center; */
  }
}
</style>
