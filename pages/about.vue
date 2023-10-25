<script setup lang="ts">
const {data} = await useFetch('/api/currency/GBP')
</script>

<template>
  <div>

    <h2>About</h2>
    <p>Lorem ipsum dolor s0it amet, consectetur adipisicing elit. Accusamus adipisci asperiores autem consectetur debitis ea eos ipsa iste iusto maxime, modi molestias nam necessitatibus numquam, obcaecati quasi sed suscipit ullam!</p>
    <p>Lorem ipsum dolor sit amet, consectetur adipisicing elit. Accusamus adipisci asperiores autem consectetur debitis ea eos ipsa iste iusto maxime, modi molestias nam necessitatibus numquam, obcaecati quasi sed suscipit ullam!</p>
    <div>
      {{data}}
    </div>
  </div>
</template>

<style scoped>
h2 {
  margin: 10px;
}
</style>

