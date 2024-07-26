<template>
  <div>
    <!-- Header Section -->
    <header class="shadow-md bg-white">
      <nav class="container mx-auto flex justify-between items-center p-4">
        <!-- Title Link -->
        <nuxt-link
          to="/products"
          class="text-xl font-bold text-gray-800 hover:text-green-600 transition-colors"
        >
          Jenjen Store Products
        </nuxt-link>
        <!-- Navigation Links -->
        <div class="hidden md:flex">
          <nuxt-link
            to="/"
            exact-active-class="text-green-600"
            class="text-gray-600 hover:text-green-600 transition-colors mx-4"
          >
            Home
          </nuxt-link>
          <nuxt-link
            to="/about"
            exact-active-class="text-green-600"
            class="text-gray-600 hover:text-green-600 transition-colors mx-4"
          >
            About
          </nuxt-link>
          <!-- <nuxt-link 
            to="/products" 
            exact-active-class="text-green-600" 
            class="text-gray-600 hover:text-green-600 transition-colors mx-4">
            Products
          </nuxt-link> -->
        </div>
      </nav>
    </header>

    <!-- Main Content Area -->
    <main class="container mx-auto p-6">
      <slot />
    </main>

    <!-- Footer Section (Navigation) -->
    <nav
      class="container mx-auto flex justify-center items-center p-4 border-t-2 border-gray-200 bg-gray-50 md:hidden"
    >
      <ul class="flex gap-6">
        <li>
          <nuxt-link
            to="/"
            exact-active-class="text-green-600"
            class="text-gray-600 hover:text-green-600 transition-colors"
          >
            Home
          </nuxt-link>
        </li>
        <li>
          <nuxt-link
            to="/about"
            exact-active-class="text-green-600"
            class="text-gray-600 hover:text-green-600 transition-colors"
          >
            About
          </nuxt-link>
        </li>
        <li>
          <nuxt-link
            to="/products"
            exact-active-class="text-green-600"
            class="text-gray-600 hover:text-green-600 transition-colors"
          >
            Products
          </nuxt-link>
        </li>
      </ul>
    </nav>
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

/* Header navigation styling */
header {
  background-color: #ffffff;
}

/* Main content area styling */
main {
  background-color: #f9f9f9;
}

/* Footer (Navigation) styling */
nav {
  background-color: #f8f8f8;
}

/* Container styling for consistent spacing */
.container {
  max-width: 1200px;
}

/* Responsive adjustments */
@media (max-width: 768px) {
  .container {
    padding-left: 1rem;
    padding-right: 1rem;
  }

  header .hidden {
    display: flex;
  }

  header .md\:flex {
    display: none;
  }
}
</style>
