<template>
  <TheHeader />
  <!-- Navigation menu -->
  <!-- Sidebar -->
  <main>
    <RouterView />
  </main>
</template>

<script setup lang="ts">
// import { RouterLink, RouterView } from 'vue-router'
import TheHeader from '@/sheets/TheHeader.vue'
import { useRoute } from 'vue-router'

const route = useRoute()
console.log(route)
</script>
<!-- 
  <style module lang="scss">
  </style> 
-->
