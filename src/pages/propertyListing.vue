<template>
  <dashboardLayout>
    <filterServices />
    <div class="main">
      <propertyList />
      <agentList />
    </div>
  </dashboardLayout>
</template>

<script setup>
import dashboardLayout from "@/layouts/dashboardLayout.vue";
import filterServices from "@/components/filter/filterServices.vue";
import propertyList from "@/components/listings/propertyList.vue";
import agentList from "@/components/agents/agentList.vue";
</script>
<style>
.main {
  display: flex;
  gap: 5px;
}
</style>
