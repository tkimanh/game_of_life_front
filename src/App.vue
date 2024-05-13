<script setup lang="ts">
import { RouterLink, RouterView } from 'vue-router'
</script>

<template>
  <head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Démo Vue</title>
  </head>
  
  <header>
    <div class="wrapper">
      <nav>
        <RouterLink to="/">Simulateur</RouterLink>
        <RouterLink to="/about">Règle</RouterLink>
      </nav>
    </div>
  </header>

  <RouterView />
</template>

<style>
  @import './assets/main.css';
</style>


