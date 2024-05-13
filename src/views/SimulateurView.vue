

<script>
export default {
  data() {
    let step = 1;

    let row = Array(10).fill(0)
    for(let i = 0; i < 10; i++)
    {
      row[i] = Array(10).fill(0)
    }

    row[4][5] = 1

    
    console.log(row)

  }
}
</script>

<template>
  <h1 class="text-red-700">Jeux de la vie</h1>
</template>