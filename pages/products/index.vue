<template>
  <div class="container mx-auto p-6">
    <h2 class="text-3xl font-bold text-gray-800 mb-6 text-center">Products</h2>
    <div class="grid grid-cols-1 sm:grid-cols-2 md:grid-cols-3 lg:grid-cols-4 gap-6">
      <div v-for="product in products" :key="product.id" class="col-span-1">
        <ProductCard :product="product" />
      </div>
    </div>
  </div>
</template>

<script setup>
import ProductCard from "~/components/ProductCard.vue";


const { data: products } = await useFetch("https://fakestoreapi.com/products");
</script>

<style scoped>
h2 {
  margin-bottom: 20px;
  font-size: 36px;
}
</style>
