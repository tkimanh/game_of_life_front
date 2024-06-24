<script setup>
import { RouterLink } from 'vue-router'

const props = defineProps(['item', 'collapsed'])
</script>

<template>
  <RouterLink :to="props.item.to">
    <div class="item">
      <div class="item__icon">
        <img
          :src="props.item.src"
          :alt="props.item.alt"
          :width="props.item.width"
          :height="props.item.height"
        />
      </div>
      <div class="item__title" v-if="!collapsed">
        {{ props.item.title }}
      </div>
    </div>
  </RouterLink>
</template>

<style scoped>
a {
  text-decoration: none;
  display: block;
  margin: var(--separacion) 0;
}

.item:hover .item__title {
  color: var(--colorNegroRelax);
  background-color: var(--colorBlancoRelax);
}

.item {
  display: flex;
  align-items: center;
  padding: var(--separacion);
  gap: var(--separacion);
}

.item__icon {
  width: 4.4rem;
  display: flex;
  justify-content: center;
  align-items: center;
}

.item__title {
  padding: 0.5rem;
  border-radius: var(--redondeo);
}
</style>
