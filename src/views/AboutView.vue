<template>
  <div class="about p-4 md:p-8">
    <h2 class="text-2xl font-bold mb-4">Règle du jeu</h2>
    <Modal
      v-show="isModalVisible"
      @close="closeModal"
    />
    <p class="mb-4">Le Jeu de la Vie est un modèle mathématique imaginé en 1970 par John Conway.</p>
      <p class="md:w-1/2 mb-4 md:mb-0 md:mr-4">
        Il s’agit d’un automate cellulaire où des cellules évoluent sur une grille bidimensionnelle à chaque tour selon des règles bien précises. <br> Une cellule peut être dans 2 états : morte ou vivante.
      </p>
      <img class="py-4 object-none" src="../assets/about/cellules.png" alt="cellule" />
 
    <p class="mb-4">
      À partir de cet état initial, notre automate peut commencer à prendre vie à travers un enchaînement de générations où nos cellules respectent 3 règles :
    </p>
    <ul class="list-disc list-inside mb-4 space-y-2">
      <li>Naissance : si une ⬛ cellule morte est entourée d’exactement 3 cellules vivantes, elle prend vie.</li>
      <li>Survie : si une ⬛ cellule vivante est entourée de 2 ou 3 🟪 vivantes, elle survit.</li>
      <li>Mort : si une ⬛ cellule vivante est entourée de moins de 2 ou plus de 3 ⬛ cellules vivantes, elle meurt (on parle de sous-population et de surpopulation).</li>
    </ul>
    <p class="mb-4">
      Chaque cellule a 8 cellules voisines hormis celles aux extrémités de la grille si celle-ci est finie.
    </p>
    <p class="mb-4">
      En enchaînant les générations, ce modèle mathématique permet de créer une simulation de la vie, avec des pixels. On parle aussi de Vie Artificielle.
    </p>
    <p class="mb-4">Voici un exemple illustrant cet automate cellulaire, sur plusieurs générations.</p>
    <img class=" mb-4" src="../assets/about/example.png" alt="exemple" />
    <p class="mb-4">Vous avez compris le principe !</p>
    <h3 class="text-xl font-semibold mb-4">4 grandes catégories de configuration</h3>
    <p class="mb-4">
      À mesure que la communauté de passionnés du jeu de la vie étudie et teste des placements de pixels et leurs évolutions, des schémas de vie se distinguent ; on parle de configurations ou « patterns ». Parmi les grandes configurations, on détaillera les 4 principales :
    </p>
    <div class="mb-4">
      <h4 class="font-semibold">Les natures mortes</h4>
      <p>Les natures mortes sont des configurations statiques. Elles ne changent pas au fil des tours.</p>
    </div>
    <div class="mb-4">
      <h4 class="font-semibold">Les oscillateurs</h4>
      <p>Les oscillateurs sont des configurations qui suivent un cycle. Elles reviennent ainsi à leur état initial après un certain nombre de générations (on parle de période).</p>
    </div>
    <div class="mb-4">
      <h4 class="font-semibold">Les vaisseaux</h4>
      <p>Les vaisseaux sont des configurations qui peuvent se déplacer. Ils agissent comme des oscillateurs qui retrouvent leur état initial à une position différente sur la grille.</p>
    </div>
    <div class="mb-4">
      <h4 class="font-semibold">Les guns</h4>
      <p>Les guns sont des configurations qui produisent, de manière répétitive, un autre type de configuration (généralement des vaisseaux). On les apparente à des usines de construction de vaisseaux.</p>
    </div>
    <div class="mb-4 flex justify-center">
      <iframe
        class="w-full md:w-2/3 h-64"
        src="https://www.youtube.com/watch?v=eMn43As24Bo"
        title="YouTube video player"
        frameborder="0"
        allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture"
        allowfullscreen
      ></iframe>
    </div>
    <h2 class="text-2xl font-bold mb-4">Histoire</h2>
    <h2 class="text-2xl font-bold mb-4">Exemples</h2>
  </div>
</template>

<script>
export default {
  name: 'About',
}
</script>

<style scoped>
/* Ajoutez des styles supplémentaires ici si nécessaire */
</style>
