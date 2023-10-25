<script setup lang="ts">
import {definePageMeta} from "#imports";
import ProductCard from "~/components/ProductCard.vue";

definePageMeta({
  layout: 'products'
})

const {data: products} = await useFetch('https://fakestoreapi.com/products')

useHead({
  title: 'Net Ninja Nuxt | Products',
  meta: [
    {name: 'description',content:'Nuxt 3 Products'}
  ]
})

</script>

<template>
  <div>
    <div class="grid grid-cols-4 gap-5">
      <div v-for="product in products">
        <ProductCard :product="product"/>
      </div>
    </div>
  </div>
</template>

<style scoped>

</style>