<template>
  <main>
    <article id="presentation">
      <div>
        <h2>Qui suis-je ?</h2>
        <p>Texte à écrire.</p>
        <p>Après plusieurs années dans le journalisme, Isabelle Raynaud a décidé de se lancer dans une nouvelle aventure professionnelle : le développement web. Cette décision est motivée par une volonté de se réinventer et de relever de nouveaux défis dans un domaine en constante évolution.</p>
        <p>Isabelle suit actuellement une formation intensive en développement web, où elle apprend les langages de programmation essentiels tels que HTML, CSS, JavaScript, ainsi que les frameworks populaires comme React et Vue.js. Sa capacité à s'adapter rapidement et à apprendre de nouvelles compétences est un atout majeur dans cette transition.</p>
        <p>En tant que future développeuse web, Isabelle Raynaud envisage d'utiliser ses compétences en journalisme et en communication pour créer des applications et des sites web qui améliorent la diffusion de l'information et l'interaction utilisateur. Elle souhaite développer des solutions innovantes qui rendent l'information plus accessible et engageante pour le public.</p>
      </div>
      <img src="../assets/images/Portrait.jpg" alt="Portrait Isabelle Raynaud">
    </article>

    <section id="creations">
      <h2>Mes créations</h2>
      <p>Mettre des cartouches cliquables</p>
      <CreationsCard></CreationsCard>
    </section>

    <section>
      <ContactForm />
    </section>
  </main>
</template>

<script setup>
import ContactForm from '../components/ContactForm.vue';
import CreationsCard from '../components/CreationsCard.vue';
</script>

<style scoped>
article {
  margin-bottom: 1rem;
  display: flex;
  flex-direction: row;
  align-items: center; 
}

img {
  width: 20%;
}
</style>