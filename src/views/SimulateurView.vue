<template>
  <div id="app">
    <div v-for="(row, rowIndex) in grid" :key="'row' + rowIndex" class="row flex">
      <div
        v-for="(cell, cellIndex) in row"
        :key="'cell' + cellIndex"
        class="cell w-[50px] h-[50px] border-[1px] border-[black]"
        :class="cell ? 'bg-black' : 'bg-white'"
        @click="updateCell(rowIndex, cellIndex)"
      ></div>
    </div>
    
  </div>
  <div @click="stepPlus(step)">
    <svg xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 24 24" stroke-width="1.5" stroke="currentColor" class="w-6 h-6">
    <path stroke-linecap="round" stroke-linejoin="round" d="M12 4.5v15m7.5-7.5h-15" />
  </svg>
</div>  
</template>

<script>
export default {
  data() {
    return {
      grid: Array(8)
        .fill()
        .map(() => Array(8).fill(false)),
      trueCells: [],
      step: 1,
    }
  },
  mounted() {
    console.log(this.grid)
  },
  
  methods: {
    updateCell(rowIndex, cellIndex) {
      this.grid[rowIndex][cellIndex] = !this.grid[rowIndex][cellIndex]

      this.grid[rowIndex][cellIndex] === true
        ? this.trueCells.push({ row: rowIndex, cell: cellIndex })
        : this.trueCells.splice(
            this.trueCells.findIndex(
              (cell) => cell.row === rowIndex && cell.cell === cellIndex
            ),
          )
    
      console.log(this.trueCells)
    },

    stepPlus(step) {
      console.log(this.grid)
      
    }
  }

}
</script>
