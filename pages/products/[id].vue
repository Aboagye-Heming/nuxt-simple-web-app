<template>
  <div>
    <p>Products details for {{ id }}</p>
  </div>
</template>

<script setup>
definePageMeta({
  layout: 'products'
})
const { id } = useRoute().params;
</script>

<style scoped></style>
