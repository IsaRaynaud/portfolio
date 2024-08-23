<template>
<div id="cards">
    <div class="creation-card" @click="showModalWindow = true">
        <h3>Capitaine Meeple</h3>
        <img alt="Capture d'écran de la page d'accueil du site Capitaine Meeple" src="./captures/CaptureCapitaineMeeple.jpg">
    </div>
    <ModalWindow v-if="showModalWindow" @close="showModalWindow = false">
        <template v-slot:title>Capitaine Meeple</template>
        <template v-slot:url><a href="https://www.capitainemeeple.com/">www.capitainemeeple.com</a></template>
        <ul>
              <li>Création en 2021</li>
              <li>Mise à jour jusqu'en 2023</li>
              <li>Utilisation de Wordpress avec Elementor</li>
        </ul>
        <template v-slot:image><img alt="Capture d'écran de la page d'accueil du site Capitaine Meeple" src="./captures/CaptureCapitaineMeeple.jpg"></template>
    </ModalWindow>
    <div class="creation-card">
        <h3>Ristretto</h3>
        <img src="./captures/CaptureRistretto.jpg" alt="Capture d'écran de la page d'accueil du site Ristretto">
    </div>
    <div class="creation-card">
        <h3>JM Développement</h3>
        <img src="./captures/Capture-jmdvlp.jpg" alt="Capture d'écran de la page d'accueil du site JM Développement">
    </div>
    <div class="creation-card">
        <h3>CV</h3>
        <img src="./captures/Capture-jmdvlp.jpg" alt="Capture d'écran de la page d'accueil du site JM Développement">
    </div>
    <div class="creation-card">
        <h3>Création de commentaires</h3>
        <img src="./captures/Capture-jmdvlp.jpg" alt="Capture d'écran de la page d'accueil du site JM Développement">
    </div>
    <div class="creation-card">
        <h3>Cahier des charges</h3>
        <img src="./captures/Capture-jmdvlp.jpg" alt="Capture d'écran de la page d'accueil du site JM Développement">
    </div>
</div>
    
</template>

<script>
import ModalWindow from './ModalWindow.vue';

export default {
    name: 'CreationsCard',
    components: {
    ModalWindow,
  },
  data() {
    return {
      showModalWindow: false,
    };
  },
};
</script>

<style scoped>
#cards {
    display: grid;
    grid-template-columns: 1fr 1fr 1fr;
}

.creation-card {
    padding: 1rem;
    width: 350px;
    cursor: pointer;
    border: 1px solid #67507C;
    margin: 1rem 0.5rem;
    display: grid;
    place-items: center;
  }
  
.creation-card:hover {
    transform: scale(1.01);
    box-shadow: 3px 3px 10px 0 #0A080C;
  }

</style>