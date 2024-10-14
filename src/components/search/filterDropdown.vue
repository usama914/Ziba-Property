<template>
  <select class="filter-dropdown" id="cars">
    <option selected disabled>Select</option>
    <option value="1">Option 1</option>
    <option value="2">Option 2</option>
    <option value="3">Option 3</option>
  </select>
</template>

<script>
export default {
  name: "FilterDropdown",
};
</script>

<style scoped>
.filter-dropdown {
  width: 100%;
  padding: 0.5rem;
  border: 1px solid #ddd;
  border-radius: 4px;
}

button.btn.dropdown-toggle {
  border: 1px solid black;
  border-radius: 0px;
  width: 100%;

  display: flex;
  justify-content: space-between;
  align-items: center;
}
</style>
