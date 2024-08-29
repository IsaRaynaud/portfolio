<template>  
    <div>
        <router-link to="/">
            <img alt="Logo Le Web plus chouette" class="logo" src="../assets/images/LogoSymbol400x300.jpg" width="300" height="225"/>
            <h1>Le web plus chouette</h1>
        </router-link>
        <nav>
            <a href="#presentation">Présentation</a>
            <a href="#creations">Créations</a>
            <a href="#contact">Contact</a>
        </nav>
    </div>
</template>

<script setup>
import { RouterLink } from 'vue-router'

</script>

<style scoped>
div {
    background-color: var(--vt-c-purple);
    margin-bottom: 2rem;
}

h1 {
  color: white;
  text-align: center;
}

a{
  text-decoration: none;
}

.logo {
    display: block;
    margin: 0 auto 2rem;
  }

nav {
    width: 100%;
    color: white;
    font-size: 1.2rem;
    text-align: center;
    margin-top: 1rem;
    padding-bottom: 1rem;
    display: flex;
    flex-direction: row;
    justify-content: center;
  }
  
nav a.router-link-exact-active {
    color: white;
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