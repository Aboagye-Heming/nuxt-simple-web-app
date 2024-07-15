<template>
  <div>
    <header class="shadow-sm bg-white">
      <nav class="container mx-auto  p-4">
        <nuxt-link to="/products" class="font-bold">Jenjen Store Products</nuxt-link>
      </nav>
    </header>
  </div>

  <div class="container mx-auto p-4">
    <slot />
  </div>
  <footer class="container mx-auto flex justify-between p-4 border-t-2">
    <ul class="flex gap-4">
      <li>
        <nuxt-link to="/">Home</nuxt-link>
      </li>
      <li>
        <nuxt-link to="/about">About</nuxt-link>
      </li>
      <li>
        <nuxt-link to="/products">Products</nuxt-link>
      </li>
    </ul>
  </footer>
</template>
<style scoped>
.router-link-exact-active {
  color: #12b488;
}
</style>
