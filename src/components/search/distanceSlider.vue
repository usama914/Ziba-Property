<template>
  <div class="distance-slider">
    <label for="distance">Distance:</label>
    <input
      type="range"
      id="distance"
      min="0"
      max="50"
      v-model="distance"
      @input="$emit('distance-change', distance)"
    />
    <div class="text-center">
      <p>{{ distance }} km</p>
    </div>
  </div>
</template>

<script>
export default {
  name: "DistanceSlider",
  data() {
    return {
      distance: 10,
    };
  },
};
</script>

<style scoped>
p {
  color: #7c7e7f;
  margin: 0px !important;
}
label{
  font-size: 12px;
}
input[type="range"] {
  width: 100%;
}
</style>
