<template>
  <div class="search-bar">
    <div class="d-flex justify-content-between align-items-center gap-2 ">
      <filterDropdown />
      <input type="text" placeholder="Search..." v-model="searchQuery" />
    </div>
    <div class="d-flex justify-content-between align-items-center gap-2">
      <div class="d-flex justify-content-between align-items-center gap-1" style="width: 100%;">
        <filterDropdown />
        <filterDropdown />
        <filterDropdown />
      </div>
      <div class="" style="width: 100%;">
        <distanceSlider />
      </div>
    </div>
  </div>
</template>

<script setup>
import { ref } from "vue";
import distanceSlider from "./distanceSlider.vue";
import filterDropdown from "./filterDropdown.vue";

const searchQuery = ref("");
</script>

<style scoped>
.search-bar {
  display: flex;
  flex-direction: column;
}
input {
  width: 100%;
  padding: 0.5rem;
  border: 1px solid #ddd;
  border-radius: 4px;
}
</style>
