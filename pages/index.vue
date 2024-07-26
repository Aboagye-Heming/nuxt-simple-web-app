<template>
  <div class="container mx-auto p-6">
    <div class="text-center my-10">
      <h2 class="text-4xl font-bold text-gray-800 mb-4">Welcome to Jenjen Store</h2>
      <p class="text-lg text-gray-600 mb-8">
        Discover our amazing collection of products tailored to meet your needs.
      </p>
      <nuxt-link 
        to="/products" 
        class="bg-green-500 text-white py-2 px-4 rounded-full hover:bg-green-600 transition-colors"
      >
        Browse Products
      </nuxt-link>
    </div>

    <div class="grid grid-cols-1 sm:grid-cols-2 lg:grid-cols-3 gap-8">
      <div class="p-6 border rounded-lg shadow hover:shadow-md transition-shadow">
        <h3 class="text-xl font-semibold text-gray-800 mb-2">Quality Products</h3>
        <p class="text-gray-600">
          Our products are of the highest quality, ensuring durability and reliability.
        </p>
      </div>
      <div class="p-6 border rounded-lg shadow hover:shadow-md transition-shadow">
        <h3 class="text-xl font-semibold text-gray-800 mb-2">Affordable Prices</h3>
        <p class="text-gray-600">
          We offer competitive prices on all our products without compromising on quality.
        </p>
      </div>
      <div class="p-6 border rounded-lg shadow hover:shadow-md transition-shadow">
        <h3 class="text-xl font-semibold text-gray-800 mb-2">Customer Support</h3>
        <p class="text-gray-600">
          Our customer support team is always here to help you with any queries.
        </p>
      </div>
    </div>
  </div>
</template>

<script setup></script>

<style scoped>
.container {
  max-width: 1200px;
}
</style>
