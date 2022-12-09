<template>
  <div class="relative top-48 flex flex-col items-center">
    <h1 class="font-heading font-bold text-3xl p-10">{{heading}}</h1>
    <slot></slot>
  </div>
</template>

<script setup>
  const props = defineProps({
    heading: {
      type: String,
      default: 'Products'
    }
  })
</script>