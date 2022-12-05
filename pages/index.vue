<template>
  <div class="body">
    <TheNav />
    <TheHero />
    <AppSection heading="LIMITED EDITION COLLECTION">
      <div class="flex flex-wrap gap-10 justify-center relative">
        <div v-for="p in products" class="md:w-1/4 w-48">
          <AppCard :product="p" />
        </div>
      </div>
    </AppSection>

    <div class="hero-footer pt-10 pb-10">
      <img src="../assets/images/footer-hero-2.jpg" alt="" />
      <img src="../assets/images/hero.jpg" alt="" />
      <img src="../assets/images/footer-hero-4.jpg" alt="" />
    </div>

    <TheFooter />
  </div>
</template>

<script setup>
const { data: products } = await useFetch("https://fakestoreapi.com/products");
</script>

<style>
.body {
  min-height: 100vh;
  display: flex;
  flex-direction: column;
}

.hero-footer {
  display: flex;
  flex-wrap: wrap;
  justify-content: center;
  width: 100%;
  position: relative;
  top: 250px;
}

.hero-footer img {
  max-width: 400px;
  min-width: 200px;
}

/* .doormat {
  width: 100%;
  height: 2.5rem;
  margin-top: auto;
} */
</style>
