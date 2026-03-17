<script setup lang="ts">
import Header from './components/Header.vue'
import Footer from './components/Footer.vue'
import { RouterView } from 'vue-router'
</script>

<template>
  <div class="app">
    <Header />
    <RouterView />
    <Footer />
  </div>
</template>

<style scoped>
.app {
  background-color: #192955;
}
</style>