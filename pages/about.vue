<template>
  <div class="container mx-auto p-6">
    <div class="text-center my-10">
      <h2 class="text-4xl font-bold text-gray-800 mb-4">About Us</h2>
      <p class="text-lg text-gray-600 mb-8">
        Welcome to Jenjen Store! We are committed to providing top-quality products and excellent customer service.
      </p>
    </div>

    <div class="bg-white p-8 rounded-lg shadow-lg">
      <p class="text-gray-800 mb-4">
        At Jenjen Store, we believe in offering a wide range of products that meet the highest standards of quality and durability. Our team works tirelessly to curate a selection of items that cater to the diverse needs of our customers.
      </p>
      <p class="text-gray-800 mb-4">
        Our mission is to enhance your shopping experience by providing exceptional service, fast shipping, and a user-friendly platform. We are dedicated to ensuring that every customer is satisfied with their purchase and enjoys shopping with us.
      </p>
      <p class="text-gray-800">
        {{ data.message }}
      </p>
    </div>
  </div>
</template>

<script setup>
const { data } = await useFetch("/api/test");
</script>

<style scoped>
.container {
  max-width: 1200px;
}
</style>
