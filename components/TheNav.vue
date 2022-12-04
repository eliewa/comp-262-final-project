<template>
  <div>
    <header class="fixed font-heading bg-black text-white text-2xl p-3 text-center">
      <p>FREE SHIPPING WORLDWIDE</p>
    </header>
    <nav class="flex justify-around container font-heading fixed top-14 p-4 text-lg bg-white">
      <div class="flex md:justify-left gap-10 items-center">
        <div class="text-3xl">
          <button @click.prevent="menuToggle">
            <Icon class="lg:invisible" name="fa6-solid:bars" />
          </button>
          <div v-show="showMenu" class="nav-links-white flex flex-col">
            <ul
              class="absolute text-center text-white text-lg mt-5 bg-black p-4 w-[80%]"
            >
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
            </ul>
          </div>
        </div>

        <TheLogo />
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
        <input type="text" name="search" id="search" placeholder="Search..." class="border-black border-2 p-1 w-1/2 invisible md:visible rounded-md">
        <Icon name=fa6-solid:magnifying-glass class="text-2xl"/>
        <p>Login</p>
        <Icon name="fa6-solid:user-large" />
      </div>
    </nav>
  </div>
</template>

<script setup>
const showMenu = ref(false);
const menuToggle = () => (showMenu.value = !showMenu.value);
</script>

<style>
  nav {
    z-index: 20;
  }
  nav .nav-links ul li::after{
  /* hover styling */
  content: '';
  width: 0;
  height: 2px;
  background: black;
  display: block;
  margin: auto;
  transition: 0.5s;
}

nav .nav-links ul li:hover::after{
  /* hover styling */
  width: 100%;
}

nav .nav-links-white ul li::after{
  /* hover styling */
  content: '';
  width: 0;
  height: 2px;
  background: white;
  display: block;
  margin: auto;
  transition: 0.5s;
}

nav .nav-links-white ul li:hover::after{
  /* hover styling */
  width: 15%;
}
</style>
