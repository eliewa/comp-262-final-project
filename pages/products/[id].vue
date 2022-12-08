<template>
  <div>
    <TheNav />
    <div class="flex w-[80%] mx-auto relative top-60 gap-14 flex-wrap md:flex-nowrap">
      <img :src="product.image" alt="product" class="lg:w-96 w-64 object-contain" />
      <div>
        <p class="pb-5 font-heading font-bold text-xl">{{ product.title }}</p>
        <p class="text-xl">$ {{ product.price }}</p>
        <p class="leading-8 font-sans py-10">
          {{ product.description }}
        </p>
        <label for="quantity" class="font-sans mr-5 font-bold">Quantity</label>
        <select name="size" id="size" class="text-xl px-4 border-2">
          <option value="">
            0
          </option>
          <option value="">
            1
          </option>
          <option value="">
            2
          </option>
          <option value="">
            3
          </option>
          <option value="">
            4
          </option>
        </select>
        <TheButton class="mb-14" />
      </div>
    </div>

    
  </div>
</template>

<script setup>
const { id } = useRoute().params;
const uri = "https://fakestoreapi.com/products/" + id;

const { data: product } = await useFetch(uri);
definePageMeta({
  layout: "products",
});
</script>
