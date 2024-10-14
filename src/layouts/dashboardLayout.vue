<template>
  <div>
    <header>
      <headerLayout />
      <nav>
        <slot />
      </nav>
    </header>
    <main>
      <router-view />
    </main>
  </div>
</template>
<script setup>
import headerLayout from "@/components/layouts/header.vue";
</script>
