<template>
  <div class="mx-auto p-4 max-w-4xl">
    <div class="grid grid-cols-1 md:grid-cols-2 gap-10">
      <div class="p-7">
        <img
          :src="productDetails.image"
          alt="product Img"
          class="mx-auto my-7 max-w-full h-auto"
        />
      </div>
      <div class="p-7">
        <h2 class="text-4xl my-7">
          {{ productDetails.title }}
        </h2>
        <p class="text-xl my-7">Price - ${{ productDetails.price }}</p>
        <h3 class="font-bold border-b-2 mb-4 pb-2">Product description:</h3>
        <p class="mb-7">{{ productDetails.description }}</p>
        <button
          class="btn flex items-center justify-center bg-green-600 text-white px-4 py-2 rounded-md hover:bg-green-700 transition-colors"
        >
          <i class="material-icons mr-2">add_shopping_cart</i>
          <span>Add to Cart</span>
        </button>
      </div>
    </div>
  </div>
</template>

<script setup>
const { id } = useRoute().params;
const url = `https://fakestoreapi.com/products/${id}`;

const { data: productDetails } = await useFetch(url, { key: id });

if (!productDetails.value) {
  throw createError({
    statusCode: 404,
    statusMessage: "Product not found",
    fatal: true,
  });
}
</script>

<style scoped>
img {
  max-width: 100%;
  height: auto;
}
</style>
