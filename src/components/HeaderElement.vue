<script setup>
import { RouterLink } from 'vue-router'

</script>

<template>  
    <div>
        <RouterLink to="/home">
            <img alt="Logo Le Web plus chouette" class="logo" src="../assets/images/logo.png" width="200" height="140"/>
        </RouterLink>
        <nav>
            <a href="/#">Présentation</a>
            <a href="/#">Création</a>
            <a href="/#">Contact</a>
        </nav>
    </div>
</template>

<style scoped>
div {
    background-color: #67507C;
    margin-bottom: 3 rem;
}

.logo {
    display: block;
    margin: 0 auto 2rem;
  }

nav {
    width: 100%;
    font-size: 1.2rem;
    text-align: center;
    margin-top: 2rem;
  }
  
nav a.router-link-exact-active {
    color: var(--color-text);
  }
  
nav a.router-link-exact-active:hover {
    background-color: transparent;
  }
  
nav a {
    color: white;
    display: inline-block;
    padding: 0 1rem;
    border-left: 1px solid var(--color-border);
  }
  
nav a:first-of-type {
    border: 0;
  }
</style>