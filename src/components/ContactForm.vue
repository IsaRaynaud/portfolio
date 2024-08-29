<template>
    <div class="contact-form">
      <form @submit.prevent="sendEmail">
        <div>
          <label for="name">Nom :</label>
          <input type="text" id="name" v-model="form.name" required>
        </div>
        <div>
          <label for="email">E-mail :</label>
          <input type="email" id="email" v-model="form.email" required>
        </div>
        <div>
          <label for="message">Message :</label>
          <textarea id="message" v-model="form.message" required></textarea>
        </div>
        <button type="submit">Envoyer</button>
      </form>
    </div>
  </template>
  
  <script>
  import emailjs from 'emailjs-com';
  
  export default {
    data() {
      return {
        form: {
          name: '',
          email: '',
          message: ''
        }
      };
    },
    methods: {
      sendEmail() {
        const serviceID = 'service_3rgcfmp';
        const templateID = 'template_sihdxre';
        const userID = 'TL6pbcIbNwOQHIBnl';
  
        emailjs.send(serviceID, templateID, this.form, userID)
          .then(response => {
            console.log('SUCCESS!', response.status, response.text);
            alert('Votre message a bien été envoyé.');
            // Réinitialiser le formulaire après la soumission
            this.form.name = '';
            this.form.email = '';
            this.form.message = '';
          })
          .catch(error => {
            console.error('FAILED...', error);
            alert("Votre message n'a pas été envoyé. Réessayez.");
          });
      }
    }
  };


  </script>
  
  <style scoped>
  h2 {
    color: #fff;
    font-weight: bold;
  }


  .contact-form {
    max-width: 750px;
    margin: 0 auto;
    padding: 1em;
    background: #AF9BBF;
    border-radius: 5px;
  }
  .contact-form div {
    margin-bottom: 1em;
  }
  .contact-form label {
    margin-bottom: .5em;
    color: #333333;
    display: block;
  }
  .contact-form input,
  .contact-form textarea {
    border: 1px solid #CCCCCC;
    padding: .5em;
    font-size: 1em;
    width: 100%;
    box-sizing: border-box;
  }
  .contact-form button {
    padding: 0.7em;
    color: black;
    background-color: #FAC748;
    border-radius: 5px;
    cursor: pointer;
  }
  .contact-form button:disabled {
    background-color: #CCCCCC;
  }
  </style>