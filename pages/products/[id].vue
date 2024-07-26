<template>
  <div>
    <p>{{ productDetails.title }}</p>
    <p>{{ productDetails.price }}</p>
    <p>{{ productDetails.id }}</p>
  </div>
</template>

<script setup>
definePageMeta({
  layout: "products",
});
const { id } = useRoute().params;
const url = `https://fakestoreapi.com/products/${id}`;

const { data: productDetails } = await useFetch(url, { key: id });
console.log(productDetails);
</script>

<style scoped></style>
