<template>
  <div>
    <header>
      <nav>
        <nuxt-link to="/">Jenjen Store</nuxt-link>
        <ul>
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
      </nav>
    </header>
  </div>

  <div>
    <slot/>
  </div>
</template>
<style scoped>
.router-link-exact-active{
    color: #12b488;
}
</style>
