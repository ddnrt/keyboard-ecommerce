<script setup>
import { RouterView } from 'vue-router'
import TheNavbar from "./components/TheNavbar.vue"
</script>

<template>
  <header>
    <div>
      <TheNavbar />
    </div>
  </header>
  <div class="mx-40">
    <RouterView />
  </div>
  
</template>

<style scoped>

</style>
