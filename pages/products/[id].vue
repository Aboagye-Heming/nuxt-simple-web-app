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
        <p class="text-xl my-7">Price- ${{ productDetails.price }}</p>
        <h3 class="font-bold border-b-2 mb-4 pb-2">Product description:</h3>
        <p class="mb-7">{{ productDetails.description }}</p>
        <button class="btn flex">
          <i class="material-icons mr-2">add_shopping_cart</i>
          <span>Add to Cart</span>
        </button>
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

if (!productDetails.value) {
  throw createError({
    statusCode: 404,
    statusMessage: "product not found",
    fatal: true,
  });
}
</script>

<style scoped>
img {
  max-width: 400px;
}
</style>
