<script setup>
import {RouterView } from 'vue-router'
import HeaderElement from './components/HeaderElement.vue';
import FooterElement from './components/FooterElement.vue';
</script>

<template>
  <header>
    <HeaderElement />
  </header>

  <RouterView />

  <footer>
    <FooterElement />
  </footer>
</template>

<style scoped>

</style>
