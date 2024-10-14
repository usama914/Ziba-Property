<template>
  <div class="property-list">
    <nav class="navbar">
      <div class="container-fluid property-display">
        <span class="navbar-text text-white"
          >144 Properties listing shown
        </span>
        <div class="d-flex justify-content-between align-items-center gap-2">
          <select id="cars">
            <option disabled selected>Sort By</option>
            <option value="asc">Ascending</option>
            <option value="desc">Descending</option>
          </select>
          <img src="../../assets/display.png" alt="" />
        </div>
      </div>
    </nav>
    <propertyCard
      v-for="property in properties"
      :key="property.id"
      :property="property"
    />
  </div>
</template>
<script setup>
// import { onMounted } from "vue";

import { usePropertyStore } from "@/stores/propertyStore";
import propertyCard from "./propertyCard.vue";

const { properties } = usePropertyStore();
// onMounted(() => {
//   properties.fetchProperties();
// });
</script>

<style scoped>
img {
  width: 50px;
}
.property-list {
  display: flex;
  flex-direction: column;
  gap: 1rem;
}
.property-display {
  background-color: #00315e;
  color: white;
  display: flex !important;
  justify-content: space-between;
}
.dropdown {
  color: white !important;
}
select {
  word-wrap: normal;
  width: 100px;
  color: white;
  background: #044d90;
  border: 0px;
  border-radius: 5px;
  padding: 2px 5px;
}
</style>
