<script setup>
</script>

<template>  
    <img alt="Vue logo" class="logo" src="../assets/images/logo.png" width="200" height="140" />
    <nav>
        <a href="/#">Présentation</a>
        <a href="/#">Création</a>
        <a href="/#">Contact</a>
    </nav>
</template>

<style scoped>
.logo {
    display: block;
    margin: 0 auto 2rem;
  }

  nav {
    width: 100%;
    font-size: 12px;
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
    display: inline-block;
    padding: 0 1rem;
    border-left: 1px solid var(--color-border);
  }
  
  nav a:first-of-type {
    border: 0;
  }
</style>