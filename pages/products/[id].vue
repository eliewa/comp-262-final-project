<template>
  <div>
    <TheNav />
    <AppSection>
        <p class="pb-10 font-sans text-xl">{{product.title}}</p>
        <img :src="product.image" alt="product" class="lg:w-96 w-64">
        <p class="lg:w-[30%] w-[80%] leading-8 font-sans pt-10">{{product.description}}</p>
        <p>$ {{product.price}}</p>
        <TheButton class="mb-14"/>
      
    </AppSection>
    
  </div>
</template>

<script setup>
  const {id} = useRoute().params;
  const uri = 'https://fakestoreapi.com/products/' + id;

  const {data: product} = await useFetch(uri);
  definePageMeta({
    layout: "products"
  })
</script>