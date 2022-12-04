<template>
  <div>
    <nav>
      <nav class="flex justify-around container">
        <div class="flex md:justify-left gap-10 items-center">
          <div class="text-3xl">
          <button @click.prevent="menuToggle"><Icon class="md:invisible" name="fa6-solid:bars" /></button>
          <div v-show="showMenu" class="flex flex-col">
            <ul class="absolute text-black text-lg mt-5 bg-gray-50 p-4 border-slate-200 border-2 font-semibold ">
              <li class="hover:underline"><NuxtLink to="/">Home</NuxtLink></li>
              <li class="hover:underline"><NuxtLink to="/products">Shop</NuxtLink></li>
              <li class="hover:underline"><NuxtLink to="/about">About</NuxtLink></li>
              <li class="hover:underline"><NuxtLink to="/blog">blog</NuxtLink></li>
            </ul>
          </div>
        </div>

        <TheLogo />
        <ul class="hidden md:flex gap-10">
          <li class="hover:text-yellow-500"><NuxtLink to="/">Home</NuxtLink></li>
          <li class="hover:text-yellow-500"><NuxtLink to="/products">Shop</NuxtLink></li>
          <li class="hover:text-yellow-500"><NuxtLink to="/about">About</NuxtLink></li>
          <li class="hover:text-yellow-500"><NuxtLink to="/blog">Blog</NuxtLink></li>
        </ul>
        </div>
        
        <div class="flex gap-4 items-center">
          <p>Login</p>
          <Icon name="fa6-solid:user-large"/>
        </div>
        
      </nav>
    </nav>
  </div>
</template>

<script setup>

</script>