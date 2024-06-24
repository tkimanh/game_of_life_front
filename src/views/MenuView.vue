<script setup>
import { ref } from 'vue'
import menuItems from './../js/MenuItems.js'
import MenuItem from './MenuItemView.vue'

let collapsed = ref(false)
</script>

<template>
  <aside :class="['menu', collapsed ? 'collapsed' : 'expanded']">
    <div class="header">
      <button class="menu-button" @click.prevent="collapsed = !collapsed">
        <img
          width="30"
          height="30"
          src="https://img.icons8.com/ios-glyphs/30/menu--v3.png"
          alt="Bouton menu"
        />
      </button>
    </div>

    <div class="menu__item">
      <ul>
        <MenuItem
          v-for="item in menuItems.items"
          :key="item.id"
          :item="item"
          :collapsed="collapsed"
        />
      </ul>
    </div>
  </aside>
</template>

<style scoped>
.menu {
  background-color: #ff5555;
  height: 100vh;
  transition: width 0.3s;
  left: 0;
  top: 0;
}

.collapsed {
  width: 5rem;
  /* height: 4.4rem; */
}

.expanded {
  width: 15rem;
  background-color: #ff5555;
}

.header {
  margin: 0 auto;
  display: flex;
  justify-content: end;
}

.menu-button {
  width: 4.4rem;
  height: 4.4rem;
  border: none;
  background-color: transparent;
  margin: 0 auto;
  display: flex;
  justify-content: center;
  align-items: center;
}

.profile {
  display: flex;
  padding: var(--separacion);
  gap: var(--separacion);
  align-items: center;
}

.profile__img {
  width: 4.4rem;
}

.profile__name {
  text-align: center;
}

.profile__name a {
  text-decoration: none;
  text-transform: capitalize;
}

.menu__item ul {
  padding: 0;
  list-style: none;
  margin: 0;
}
</style>
