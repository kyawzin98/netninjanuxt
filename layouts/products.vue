<template>
  <div>
    <header class="shadow-sm bg-white">
      <nav class="container mx-auto p-4">
        <NuxtLink class="font-bold" to="/products">Net Ninja Nuxt | Products</NuxtLink>
      </nav>
    </header>

    <!--  Page Content  -->
    <div class="container mx-auto p-4">
      <slot/>
    </div>

    <footer class="container mx-auto p-4 flex justify-between border-t">
      <ul class="flex gap-4">
        <li>
          <NuxtLink to="/">Home</NuxtLink>
        </li>
        <li>
          <NuxtLink to="/about">About</NuxtLink>
        </li>
        <li>
          <NuxtLink class="btn" to="/products">Products</NuxtLink>
        </li>
      </ul>
    </footer>
  </div>
</template>


<style scoped>
//.router-link-exact-active {
//  //color: #12b488
//}
</style>
<script setup lang="ts">
</script>