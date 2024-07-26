<template>
  <div>
    <!-- Header Section -->
    <header class="shadow-md bg-white fixed top-0 left-0 w-full z-10">
      <nav class="container mx-auto flex justify-between items-center p-4">
        <!-- Brand Link -->
        <nuxt-link to="/" class="text-2xl font-bold text-gray-800 hover:text-green-600 transition-colors">
          Jenjen Store
        </nuxt-link>

        <!-- Navigation Links -->
        <ul class="hidden md:flex gap-6">
          <li>
            <nuxt-link to="/" exact-active-class="text-green-600" class="text-gray-600 hover:text-green-600 transition-colors">
              Home
            </nuxt-link>
          </li>
          <li>
            <nuxt-link to="/about" exact-active-class="text-green-600" class="text-gray-600 hover:text-green-600 transition-colors">
              About
            </nuxt-link>
          </li>
          <li>
            <nuxt-link to="/products" exact-active-class="text-green-600" class="text-gray-600 hover:text-green-600 transition-colors">
              Products
            </nuxt-link>
          </li>
        </ul>

        <!-- Mobile Menu Toggle Button -->
        <button @click="toggleMenu" class="md:hidden text-gray-600 hover:text-green-600 transition-colors">
          <span :class="{ 'hidden': menuOpen, 'block': !menuOpen }">☰</span>
          <span :class="{ 'block': menuOpen, 'hidden': !menuOpen }">✕</span>
        </button>
      </nav>

      <!-- Mobile Navigation Links -->
      <ul v-if="menuOpen" class="md:hidden flex flex-col items-center gap-4 p-4 bg-gray-50 border-t border-gray-200">
        <li>
          <nuxt-link to="/" exact-active-class="text-green-600" class="text-gray-600 hover:text-green-600 transition-colors" @click="toggleMenu">
            Home
          </nuxt-link>
        </li>
        <li>
          <nuxt-link to="/about" exact-active-class="text-green-600" class="text-gray-600 hover:text-green-600 transition-colors" @click="toggleMenu">
            About
          </nuxt-link>
        </li>
        <li>
          <nuxt-link to="/products" exact-active-class="text-green-600" class="text-gray-600 hover:text-green-600 transition-colors" @click="toggleMenu">
            Products
          </nuxt-link>
        </li>
      </ul>
    </header>

    <!-- Main Content -->
    <main class="container mx-auto p-6 mt-24">
      <slot />
    </main>
  </div>
</template>

<script setup>
import { ref } from 'vue';

const menuOpen = ref(false);
const toggleMenu = () => {
  menuOpen.value = !menuOpen.value;
};
</script>

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

/* Mobile menu toggle styling */
button {
  font-size: 24px;
  cursor: pointer;
}
</style>
