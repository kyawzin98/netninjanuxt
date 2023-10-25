<script setup lang="ts">
import {definePageMeta} from "#imports";

const {id} = useRoute().params

const uri = 'https://fakestoreapi.com/products/' + id;

// fetch product detail
const {data: product} = await useFetch(uri)

if (!product.value){
  throw createError({statusCode: 404, statusMessage: 'Product not found', fatal: true})
}

definePageMeta({
  layout: 'products'
})
</script>

<template>
  <div>
    <Head>
      <Title>Net Ninja Nuxt | {{product.title}}</Title>
      <Meta name="description" :content="product.description"></Meta>
    </Head>
    <ProductDetails :product="product"/>
  </div>
</template>

<style scoped>

</style>