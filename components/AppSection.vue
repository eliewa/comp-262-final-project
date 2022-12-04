<template>
  <div>
    <h1 class="font-heading font-bold text-3xl">{{heading}}</h1>
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