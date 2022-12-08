<template>
  <div>
    <TheNav class="pb-56"/>
    <AppBlogSection 
    :image="section.image"
    :alt="section.alt"
    :heading="section.heading"
    :text="section.text"
    v-for="section in sections" 
    :key="section.id"
    />
    <TheFooter />
  </div>
</template>

<script setup>
useHead({
  title: 'RAW Industries | Blog'
})
  const sections = [
    {
      id: 1,
      image: "images/footer-hero-1.jpg",
      alt: "Image of girl",
      heading: "Best street art locations in town",
      text: "There are unlimited street art locations around Calgary, here is a list of all the best markets around the area in 2023!....",
    },

    {
      id:2,
      image: "/images/footer-hero-2.jpg",
      alt: "Image of boy",
      heading: "5 hot trends in street fashion",
      text: "New trends are created everyday, why not get yourself up to date with the 5 hottest trends happening now!....",
    },

    {
      id:4,
      image: "/images/footer-hero-3.jpg",
      alt: "Image of boy",
      heading: "10 Things to know when shopping",
      text: "Read this article to find out about some tips and tricks about how to shop effectively and efficiently....",
    },

    { id:5,
      image: "/images/footer-hero-4.jpg",
      alt: "Image of boy",
      heading: "Goodbye Summer, Hello Winter",
      text: "Out with the summer in with the winter, get ready to take control of this winter!....",
    },
  ]
</script>

