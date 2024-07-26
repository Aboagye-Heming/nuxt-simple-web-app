<template>
  <div class="card">
    <div class="grid grid-cols-2 gap-10">
      <div class="p-7">
        <img
          :src="productDetails.image"
          alt="product Img"
          class="mx-auto my-7"
        />
      </div>
      <div class="p-7">
        <h2 class="text-4xl my-7">
          {{ productDetails.title }}
        </h2>
        <p class="text-xl my-7">Price- ${{ productDetails.price }} </p>
        <h3 class="font-bold border-b-2 mb-4 pb-2">Product description: </h3>
        <p class="mb-7">{{ productDetails.description }}</p>
      </div>
    </div>
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

<style scoped>
img{
  max-width: 400px;
}
</style>
