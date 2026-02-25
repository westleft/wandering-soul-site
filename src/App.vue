<script setup lang="ts">
import Header from './components/Header.vue'
import { RouterView } from 'vue-router'
</script>

<template>
  <div class="app">
    <Header />
    <RouterView />
  </div>
</template>

<style scoped>
.app {
  background-color: #192955;
}
</style>