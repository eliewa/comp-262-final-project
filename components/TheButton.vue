<template>
  <div class="mt-7 font-sans border-2 p-2">
    {{btnInfo}}
  </div>
</template>

<script setup>
  const props = defineProps({
    btnInfo: {
      type: String,
      default: 'Add to Cart'
    }
  })
</script>
