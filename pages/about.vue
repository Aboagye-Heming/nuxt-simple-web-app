<template>
  <div>
    <h2>About</h2>
    <p>
      Lorem ipsum dolor sit amet consectetur adipisicing elit. Iusto officia
      culpa, sapiente ducimus possimus expedita quae sed delectus debitis
      repellat sequi! A similique natus veniam perferendis neque unde ea hic.
    </p>
    <p>
      {{ data.message }}
    </p>
  </div>
</template>

<script setup>
const { data } = await useFetch("/api/test");
</script>

<style scoped>
h2 {
  margin-bottom: 20px;
  font-size: 36px;
}
p {
  margin: 20px 0;
}
</style>
