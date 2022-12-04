<template>
  <div>
    <TheNav />
    <div class="flex flex-wrap gap-10">
    <div v-for="p in products" class="md:w-1/4 w-48">
      <AppCard :product="p"/>
    </div>
  </div>
  </div>
</template>

<script setup>
  definePageMeta({
    layout: "products"
  })
  
  const {data: products} = await useFetch('https://fakestoreapi.com/products');
</script>