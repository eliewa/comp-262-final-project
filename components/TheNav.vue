<template>
  <div>
    <header
      class="fixed font-heading bg-black text-white text-2xl p-3 text-center w-[100%]"
    >
      <p>FREE SHIPPING WORLDWIDE</p>
    </header>
    <nav
      class="fixed flex justify-around font-heading top-14 p-4 text-lg bg-white w-[100%]"
    >
      <div class="flex md:justify-left gap-10 items-center">
        <div class="text-3xl">
          <button @click.prevent="menuToggle">
            <Icon class="lg:invisible" name="fa6-solid:bars" />
          </button>
          <div v-show="showMenu" class="nav-links-white flex flex-col bg-black">
            <ul
              class="absolute text-center text-white text-lg mt-5 p-4 bg-black w-80 flex justify-between rounded-md"
            >
              <div>
                <li class="p-2"><NuxtLink to="/">Home</NuxtLink></li>
                <li class="p-2">
                  <NuxtLink to="/products">Shop</NuxtLink>
                </li>
                <li class="p-2">
                  <NuxtLink to="/about">About</NuxtLink>
                </li>
                <li class="p-2">
                  <NuxtLink to="/blog">Blog</NuxtLink>
                </li>
              </div>
              <div>
                <button @click.prevent="menuToggle">
                  <Icon name="fa6-solid:xmark" class="text-white text-2xl hover:border-2 hover:border-white" />
                </button>
                
              </div>
            </ul>
          </div>
        </div>

        <TheLogo class="hidden sm:block" />
        <div class="nav-links">
          <ul class="hidden lg:flex gap-10">
            <li>
              <NuxtLink to="/">Home</NuxtLink>
            </li>
            <li>
              <NuxtLink to="/products">Shop</NuxtLink>
            </li>
            <li>
              <NuxtLink to="/about">About</NuxtLink>
            </li>
            <li>
              <NuxtLink to="/blog">Blog</NuxtLink>
            </li>
          </ul>
        </div>
      </div>

      <div class="flex gap-4 items-center">
        <div>
          <input
            type="search"
            v-model="search"
            id="search"
            placeholder="Search..."
            class="border-black border-2 p-1 w-1/2 rounded-md"
          />
          <button
            @click.prevent="productToggle"
            type="search"
            id="search"
            class="search"
          >
            <Icon
              name="fa6-solid:magnifying-glass"
              class="text-2xl hover:border-2 border-black ml-4"
            />
          </button>
          <div v-show="showProduct">
            <div class="bg-white w-64 h-96 border-2 absolute overflow-y-scroll">
              <div v-for="p in matchingProducts" :key="p.id">
                <NuxtLink :to="link + p.id">
                  <Product
                    :title="p.title"
                    :image="p.image"
                    :price="p.price"
                    class="hover:underline"
                  />
                </NuxtLink>
              </div>
            </div>
          </div>
        </div>

        <p class="hidden md:block">Login</p>
        <Icon
          name="fa6-solid:user-large"
          class="text-xl invisible md:visible"
        />
      </div>
    </nav>
  </div>
</template>

<script setup>
const showMenu = ref(false);
const menuToggle = () => (showMenu.value = !showMenu.value);

const showProduct = ref(false);
const productToggle = () => (showProduct.value = !showProduct.value);

const search = ref("");

const { data: products } = await useFetch("https://fakestoreapi.com/products");
const link = "/products/";

const matchingProducts = computed(() => {
    return products.value.filter((product) =>
    product.title.toLowerCase().includes(search.value.toLowerCase())
  );
});
</script>

<style>
nav,
header {
  z-index: 20;
}

nav .nav-links ul li::after {
  /* hover styling */
  content: "";
  width: 0;
  height: 2px;
  background: black;
  display: block;
  margin: auto;
  transition: 0.5s;
}

nav .nav-links ul li:hover::after {
  /* hover styling */
  width: 100%;
}

nav .nav-links-white ul li::after {
  /* hover styling */
  content: "";
  width: 0;
  height: 2px;
  background: white;
  display: block;
  margin: auto;
  transition: 0.5s;
}

nav .nav-links-white ul li:hover::after {
  /* hover styling */
  width: 100%;
}
</style>
