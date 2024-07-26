<template>
  <div>
    <!-- Header Section -->
    <header class="shadow-md bg-white">
      <nav class="container mx-auto flex justify-between items-center p-4">
        <!-- Brand Link -->
        <nuxt-link to="/" class="text-2xl font-bold text-gray-800 hover:text-green-600 transition-colors">Jenjen Store</nuxt-link>
        
        <!-- Navigation Links -->
        <ul class="flex gap-6">
          <li>
            <nuxt-link to="/" exact-active-class="text-green-600" class="text-gray-600 hover:text-green-600 transition-colors">Home</nuxt-link>
          </li>
          <li>
            <nuxt-link to="/about" exact-active-class="text-green-600" class="text-gray-600 hover:text-green-600 transition-colors">About</nuxt-link>
          </li>
          <li>
            <nuxt-link to="/products" exact-active-class="text-green-600" class="btn bg-green-600 text-white px-4 py-2 rounded-md hover:bg-green-700 transition-colors">Products</nuxt-link>
          </li>
        </ul>
      </nav>
    </header>

    <!-- Main Content -->
    <main class="container mx-auto p-6">
      <slot />
    </main>
  </div>
</template>

<style scoped>
/* Styling for active navigation link */
.router-link-exact-active {
  color: #12b488;
}

/* General link styling */
a {
  text-decoration: none;
}

/* Button styling */
.btn {
  display: inline-block;
  font-weight: 600;
  text-align: center;
  border-radius: 4px;
  transition: background-color 0.3s ease;
}
</style>
