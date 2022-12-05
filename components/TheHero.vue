<template>
  <div class="hero flex text-white flex-col justify-center items-center">
    <h1 class=" font-display text-5xl w-1/2 text-center">ALWAYS BE ORIGINAL</h1>
    <p class="font-heading text-xl pt-7">NEW ARRIVALS ARE HERE</p>
    <NuxtLink to="products">
      <TheButton btn-info="SHOP NOW"/>
    </NuxtLink>
  </div>  
</template>

<script setup>

</script>

<style>
  .hero {
    background-image: linear-gradient(rgba(0, 0, 0, 0.342), rgba(0, 0, 0, 0.377)), url(../assets/images/hero.jpg) ;
    background-position: center;
    background-size: cover;
    width: 80%;
    height: 80vh;
    margin: auto;
    position: relative;
    top: 100px;
  }
</style>