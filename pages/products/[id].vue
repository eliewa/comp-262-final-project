<template>
  <div>
    <TheNav />
    <AppSection>
      <p>{{product.title}}</p>
      <img :src="product.image" alt="product" class="w-1/3">
      <p>$ {{product.price}}</p>
      <TheButton />
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