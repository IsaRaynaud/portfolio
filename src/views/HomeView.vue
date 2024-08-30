<template>
  <main>
    <article id="presentation">
      <div>
        <h2>Bienvenue !</h2>
        <p>Je m'appelle Isabelle Raynaud, et après plusieurs années passionnantes passées dans le journalisme, j'ai décidé de me lancer dans une nouvelle aventure : le développement web. Ce changement de cap est le fruit de ma volonté de relever de nouveaux défis et de m'investir dans un domaine en perpétuelle évolution.</p>
        <p>Actuellement en formatio, j'apprends les langages de programmation essentiels tels que HTML, CSS, JavaScript, ainsi que des frameworks populaires comme Vue.js. Cette formation me permet d'acquérir les compétences techniques nécessaires pour concevoir des sites web modernes, dynamiques, et adaptés aux besoins des petites entreprises et des indépendants.</p>
        <p>Ce projet, "Le Web plus chouette", est bien plus qu'une simple activité. C'est la fusion de mon expertise en communication et de mes nouvelles compétences pour le développement web. Mon objectif est de créer des sites et des applications qui non seulement répondent aux attentes techniques, mais qui sont aussi pensés pour améliorer la diffusion de l'information et l'expérience utilisateur.</p>
        <p>Je suis convaincue que chaque entreprise mérite une présence en ligne qui reflète son identité et ses valeurs. Avec "Le Web plus chouette", je suis là pour vous accompagner dans la création d'une plateforme qui vous ressemble, et qui rendra votre contenu accessible et engageant pour votre public.</p>
        <p>Merci de me faire confiance pour transformer vos idées en réalité digitale !</p>
  
      </div>
      <img src="../assets/images/Portrait.jpg" alt="Portrait Isabelle Raynaud">
    </article>

    <section id="creations">
      <h2>Mes créations</h2>
      <CreationsCard></CreationsCard>
    </section>

    <section id="contact">
      <h2>Contactez-moi</h2>
      <ContactForm />
    </section>
  </main>
</template>

<script setup>
import ContactForm from '../components/ContactForm.vue';
import CreationsCard from '../components/CreationsCard.vue';
</script>

<style scoped>
main {
  padding: 1.5rem;
}

article {
  margin-bottom: 1rem;
  display: flex;
  flex-direction: row;
  align-items: center; 
}

img {
  width: 20%;
  padding-left: 0.8rem;
}

section{
  margin-top: 2rem;
}
</style>