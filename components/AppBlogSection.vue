<template>
  <div class="card border-b-2 lg:w-[50%] mx-auto w-[80%] mb-16 p-5 pb-20">
    <img :src="image" :alt="alt" class="pb-16 w-[100%]" >
    <div class="pl-10">
      <h1 class="font-heading text-3xl font-bold pb-4">{{heading}}</h1>
      <p class="leading-8 text-lg">{{text}}</p>
    </div>
    

  </div>
</template>

<script setup>
  const props = defineProps({
    image: {
      type: String,
      default: "/images/footer-hero-1.jpg",
    },
    alt: {
      type: String,
      default: 'Blog Image'
    },
    heading: {
      type: String,
      default: 'Best street art locations in town',
    },
    text: {
      type: String,
      default: 'Create a blog post subtitle that summarizes your post in a few short, punchy sentences and entices your audience to continue reading....',
    } 
  })
</script>
  
<style scoped>
  .card img {
    height: 600px;
    object-fit: cover;
  }
</style>