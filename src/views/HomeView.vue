<script setup>
import ContactForm from '../components/ContactForm.vue';
</script>

<template>
  <main>
    <article id="presentation">
      <div>
        <h2>Qui suis-je ?</h2>
        <p>Texte à écrire</p>
      </div>
      <img src="../assets/images/Portrait.jpg" alt="Portrait Isabelle Raynaud">
    
    </article>

    <article id="creations">
      <p>Mettre des cartouches cliquables</p>
    </article>

    <ContactForm />
  </main>
</template>

<style scoped>
article {
  display: flex;
  flex-direction: row;
  align-items: center;
}

img {
  width: 20%;
}
</style>