<template>
  <div class="about">
    <h1>Connexion</h1>
    <div class="block-flex-column">
      <label for="username">Username :</label>

      <input type="text" id="username" name="username" />

      <label for="password">Mot de passe (8 charactères minimum) :</label>
      <input type="password" id="password" name="password" minlength="8" required />
    </div>
    <button class="btn-ajout-type-vaisseau">Se connecter</button>
  </div>
</template>

<script lang="ts">
import axios from '@/router/api'
import { defineComponent } from 'vue'

export default defineComponent({
  name: 'Login',
  data() {
    return {
      username: '',
      password: ''
    }
  },
  methods: {
    async login() {
      try {
        const response = await axios.post('/login', {
          username: this.username,
          password: this.password
        })
        console.log(response.data)
        // Gérer le succès de la connexion ici (par exemple, stocker le jeton JWT, rediriger l'utilisateur, etc.)
      } catch (error) {
        console.error(error)
        // Gérer les erreurs ici (par exemple, afficher un message d'erreur à l'utilisateur)
      }
    }
  }
})
</script>
