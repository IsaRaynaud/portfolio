<template>
    <div v-if="isVisible" class="modal-overlay" @click.self="closeModalWindow">
      <div class="modal-content">
          <h2><slot name="title"></slot></h2>
          <slot name="url"></slot>
          <slot></slot>
          <slot name="image"></slot>
          <button @click="closeModalWindow">Fermer</button>
      </div>
    </div>
  </template>
  
  <script>
  export default {
    props: {
    isVisible: {
      type: Boolean,
      required: true
    }
  },
  methods: {
    closeModalWindow() {
      this.$emit('close');
    }
  }
  }
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
    display: grid;
    place-items: center;
  }

  button{
    margin: 1rem;
    padding: 0.3rem;
  }
  </style>