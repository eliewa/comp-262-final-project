<template>
  <div>
    <article class="p-4 font-semibold font-sans">
      <p class="font-heading">{{title}}</p>
      <img :src="image" alt="" class="h-40 w-full mx-auto py-2 object-contain object-center">
      <p class="p-2 text-center">$ {{price}}</p>
    </article>
  </div>
</template>

<script setup>
  const props = defineProps({
    title: {
      type: String,
      default: 'Air Force 1',
    },
    image: {
      type: String,
    },
    price: {
      type: String,
      default: '129.99'
    }
  })
</script>