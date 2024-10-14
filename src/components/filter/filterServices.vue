<template>
  <div class="filter_services mb-1">
    <div class="filter-options">
      <serviceTabs />
      <searchBar />
    </div>
    <div class="map-filter">
      <mapView />
    </div>
  </div>
</template>

<script setup>
import searchBar from "@/components/search/searchBar.vue";
import serviceTabs from "../search/serviceTabs.vue";
import mapView from "../map/mapView.vue";
</script>

<style scoped>
.filter_services {
  display: flex;
  gap: 2px;
  /* border: 1px solid black; */
}
.filter-options {
  max-width: 900px;
  width: 100%;
}

</style>
