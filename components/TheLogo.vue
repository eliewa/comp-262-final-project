<template>
  <div>
    <div :class="size">
      <NuxtLink to="/">
        <span class="font-display">RAW</span>
        <span class="text-4xl">.</span>
      </NuxtLink>
    </div>
  </div>
</template>

<script setup>
const props = defineProps({
  size: {
    type: String,
    default: "text-2xl",
  },
});
</script>
