<template>
  <div class="mt-auto h-auto relative top-64 overflow-hidden">
    <footer class="bg-black text-white font-heading">
      <div class="p-4 text-center border-b border-gray-200">
        <TheLogo size="text-4xl" class="p-4 lg:relative lg:left-[30%]" />
        <div class="nav-links">
          <ul class="text-center flex md:flex-row md:gap-10 flex-col gap-4 justify-center w-28 mx-auto">
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

      <p class="text-center p-5 text">&copy; 2012 RAW Industries inc.</p>
    </footer>
  </div>
</template>

<script setup></script>

<style>

footer .nav-links ul li::after {
  /* hover styling */
  content: "";
  width: 0;
  height: 2px;
  background: white;
  display: block;
  margin: auto;
  transition: 0.5s;
}

footer .nav-links ul li:hover::after {
  /* hover styling */
  width: 90%;
}
</style>
