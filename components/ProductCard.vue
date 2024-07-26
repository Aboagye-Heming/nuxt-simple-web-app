<template>
    <div class="card text-center">
      <img :src="product.image" alt="product thumb" class="thumb" />
      <p class="font-bold text-gray-500 m-4 truncate">{{ product.title }}</p>
      <nuxt-link :to="`/products/${product.id}`">
        <p class="py-4 btn">View Details</p>
      </nuxt-link>
    </div>
  </template>
  
  <script setup>
  const props = defineProps({
    product: {
      type: Object,
      required: true
    }
  });
  </script>
  
  <style scoped>
  .thumb {
    max-width: 70%;
    max-height: 120px;
    margin: 0 auto;
  }
  </style>
  