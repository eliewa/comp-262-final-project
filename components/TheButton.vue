<template>
  <div class="mt-7 font-sans border-2 p-2 w-40 mx-auto hover:bg-black hover:text-white text-center">
    {{btnInfo}}
  </div>
</template>

<script setup>
  const props = defineProps({
    btnInfo: {
      type: String,
      default: 'View Product'
    }
  })
</script>
