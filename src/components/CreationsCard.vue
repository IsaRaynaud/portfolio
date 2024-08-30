<template>
<div id="cards">
    <div class="creation-card" 
        v-for="(card,index) in cards"
        :key="index"
        @click="showModal(index)">
        <h3>{{card.title}}</h3>
        <img :alt="card.alt" :src="card.image">
    </div>
    <!--Fenêtre modale dynamique-->
    <ModalWindow
        :isVisible="activeModal !== null"
        @close="activeModal = null">
        <template v-slot:title>{{ cards[activeModal].title }}</template>
        <template v-slot:url>
            <a :href="cards[activeModal].url" target="_blank">{{ cards[activeModal].url }}</a>
        </template>
        <ul>
            <li v-for="(info,index) in cards[activeModal].details" :key="index">{{ info }}</li>
        </ul>
        <img :alt="cards[activeModal].alt" :src="cards[activeModal].image">
    </ModalWindow>
</div>   
</template>

<script>
import ModalWindow from './ModalWindow.vue';
import CaptureCapitaineMeeple from './captures/CaptureCapitaineMeeple.jpg';
import CaptureJmdvlp from './captures/CaptureJmdvlp.jpg';
import CaptureRistretto from './captures/CaptureRistretto.jpg';
import CaptureCahierCharges from './captures/CaptureCahierCharges.jpg';
import CaptureCV from './captures/CaptureCV.jpg';
import CaptureCommentaires from './captures/CaptureCommentaires.jpg';

export default {
    name: 'CreationsCard',
    components: {
    ModalWindow,
  },
  data() {
    return {
      activeModal: null,
      cards: [
        {
            title: "Capitaine Meeple",
            alt: "Capture d'écran de la page d'accueil du site Capitaine Meeple",
            image: CaptureCapitaineMeeple,
            url: "https://www.capitainemeeple.com/",
            details: ["Création en 2021", "Mise à jour jusqu'en 2023", "Utilisation de Wordpress avec Elementor"]
        },
        {
            title: "Ristretto",
            alt: "Capture d'écran de la page d'accueil du site Ristretto",
            image: CaptureRistretto,
            url: "https://ristretto.media/",
            details: ["Création en 2023", "Utilisation de Wordpress avec Elementor"]
        },
        {
            title: 'JM Développement',
            alt: "Capture d'écran de la page d'accueil du site JM Développement",
            image: CaptureJmdvlp,
            url: 'https://jm-developpement.com/',
            details: ['Création en 2023', 'Utilisation de Wordpress avec Elementor'] 
        },
        {
            title: 'Mon CV',
            alt: "Capture d'écran de la page 'Mon CV', projet de formation",
            image: CaptureCV,
            url: 'https://github.com/IsaRaynaud/cv',
            details: ['Création en 2024', 'Utilisation de HTML et CSS'] 
        },
        {
            title: 'Page de commentaires',
            alt: "Capture d'écran du projet de création d'espace commentaires",
            image: CaptureCommentaires,
            url: 'https://github.com/IsaRaynaud/nouveau_commenatire',
            details: ['Création en 2024', 'Utilisation des codes HTML, CSS et Javascript'] 
        },
        {
            title: 'Cahier des charges',
            alt: "Capture d'écran du cahier des charges créé lors de ma formation",
            image: CaptureCahierCharges,
            url: 'https://isabelle-raynaud.fr/wp-content/uploads/2024/08/CDC-Socketterie.pdf',
            details: ['Création en 2024'] 
        }
      ]
    };
  },
  methods: {
    showModal(index) {
        this.activeModal = index;
    }
  }
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