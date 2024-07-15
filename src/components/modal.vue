<template>
    <div v-if="isVisible" class="fixed inset-0 flex items-center justify-center z-50 bg-black bg-opacity-50">
      <div class="bg-white rounded-lg shadow-lg w-11/12 md:w-1/2 p-6">
        <div class="flex justify-between items-center mb-4">
          <h2 class="text-xl font-bold">{{ title }}</h2>
          <button @click="closeModal" class="text-gray-700 hover:text-gray-900">&times;</button>
        </div>
        <div class="mb-4">
          <slot></slot>
        </div>
        <div class="flex justify-end">
          <button @click="closeModal" class="bg-blue-500 text-white px-4 py-2 rounded-lg hover:bg-blue-700">Close</button>
        </div>
      </div>
    </div>
  </template>
  
  <script>
  export default {
    name: 'Modal',
    props: {
      isVisible: {
        type: Boolean,
        required: true
      },
      title: {
        type: String,
        default: 'Modal Title'
      }
    },
    methods: {
      closeModal() {
        this.$emit('close');
      }
    }
  }
  </script>
  
  <style scoped>
  </style>
  