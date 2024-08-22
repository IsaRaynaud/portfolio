<template>
    <div class="modal-overlay" @click.self="$emit('close')">
      <div class="modal-content">
            <h2><slot name="title"></slot></h2>
            
        
          <button @click="$emit('close')">Fermer</button>
      </div>
    </div>
  </template>
  
  <script>
  export default {
    name: "Modal",
  };
  </script>
  
  <style scoped>
  .modal-overlay {
    position: fixed;
    top: 0;
    left: 0;
    width: 100%;
    height: 100%;
    background: rgba(0, 0, 0, 0.5);
    display: flex;
    justify-content: center;
    align-items: center;
  }
  
  .modal-content {
    background: white;
    padding: 2rem;
    border-radius: 1rem;
    width: 600px;
    max-width: 90%;
  }

  h2{
    text-align: center;
    font-size: larger;
  }

  p{
    text-align: center;
  }

  button{
    margin: 1rem;
    padding: 0.3rem;
    display: flex;
    justify-content: center;
  }
  </style>