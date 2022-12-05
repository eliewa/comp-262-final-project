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
    <AppSection>
      <img src="../assets/images/final-footer.jpg" alt="people" class="relative top-64" >
    </AppSection>
   
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

/* .doormat {
  width: 100%;
  height: 2.5rem;
  margin-top: auto;
} */
</style>