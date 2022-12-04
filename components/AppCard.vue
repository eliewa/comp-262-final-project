<template>
  <div class="card text-center">
    <img :src="product.image" alt="" class="h-72 object-contain mx-auto">
    <p class="font-bold text-gray-500 m-4 truncate">{{product.title}}</p>
    <NuxtLink :to="`/products/${product.id}`">
      <p class="bg-green-300 rounded-md p-4">View Details</p>
    </NuxtLink>
  </div>
</template>

<script setup>
  const {product} = defineProps([
   'product'
  ])
</script>