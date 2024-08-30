<script setup>
</script>

<template>
    <div>
        <h2>Vous êtes perdu ?</h2>
        <img alt="Image d'une personne perdue dans un labyrinthe" src="../assets/images/labyrintheNB.png">
        <p>La page que vous cherchez ne semble pas exister...</p>
        <router-link to="/">
        <button>Retourner à l'accueil</button>
        </router-link>
    </div>

</template>

<style scoped>
div {
    display: grid;
    place-items: center;
}

p{
    font-weight: bold;
}
</style>
