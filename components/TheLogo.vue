<template>
  <div>
    <div :class="size">
      <NuxtLink to="/" class="flex items-center gap-1">
        <Icon name="game-icons:chess-king" class="text-4xl relative bottom-1"/>
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
    default: "text-3xl",
  },
});
</script>
