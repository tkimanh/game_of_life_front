<template>
  <div id="app">
    <div v-for="(row, rowIndex) in grid" :key="'row' + rowIndex" class="row flex">
      <div 
        v-for="(cell, cellIndex) in row" 
        :key="'cell' + cellIndex" 
        class="cell w-[50px] h-[50px] border-[1px] border-[black]"
        @click="clickCell(row, rowIndex, cellIndex)"
      >
        
      </div>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      grid: Array(8).fill().map(() => Array(8).fill(false)) 
    }
  },
  mounted() {
    console.log(this.grid)
  },

  methods: {

    clickCell(row, rowIndex, cellIndex) {
      let gridTrrue = []
      console.log(row)  

      if (rowIndex  == false && cellIndex == false ) {
        gridTrrue.push([rowIndex, cellIndex])
        
      }
    }
  }
}
</script>
