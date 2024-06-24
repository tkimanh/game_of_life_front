<script setup>
import { RouterView } from 'vue-router'
import Menu from './views/MenuView.vue'
</script>

<template>
  <head>
    <meta charset="UTF-8" />
    <meta http-equiv="X-UA-Compatible" content="IE=edge" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <title>Démo Vue</title>
  </head>

  <div id="app">
    <Menu />

    <main id="page-wrap">
      <RouterView />
    </main>
  </div>
</template>

<style>
@import './assets/main.css';
</style>
