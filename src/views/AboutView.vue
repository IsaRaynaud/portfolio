<script setup>
import HeaderElement from '../components/HeaderElement.vue'
import FooterElement from '../components/FooterElement.vue'
</script>

<template>
  <header>
    <HeaderElement />
  </header>
  <footer>
    <FooterElement />
  </footer>
</template>

<style>
footer{
  background-color: #0A080C ;
  padding: 30px 30px 30px 15px;
  display: flex;
  flex-direction: column;
  align-items: center;
}
</style>
