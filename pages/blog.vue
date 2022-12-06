<template>
  <div>
    <TheNav class="pb-56"/>
    <AppBlogSection 
    :image="section.image"
    :alt="section.alt"
    :heading="section.heading"

    v-for="section in sections" 
    :key="section.id"
    />
    <TheFooter />
  </div>
</template>

<script setup>
  const sections = [
    {
      id: 1,
      image: "images/footer-hero-1.jpg",
      alt: "Image of girl",
      heading: "Best street art locations in town",
      text: "Create a blog post subtitle that summarizes your post in a few short, punchy sentences and entices your audience to continue reading....",
    },

    {
      id:2,
      image: "/images/footer-hero-2.jpg",
      alt: "Image of boy",
      heading: "5 hot trends in street fashion",
      text: "Create a blog post subtitle that summarizes your post in a few short, punchy sentences and entices your audience to continue reading....",
    },

    {
      id:4,
      image: "/images/footer-hero-3.jpg",
      alt: "Image of boy",
      heading: "Our new downtown pop-up store",
      text: "Create a blog post subtitle that summarizes your post in a few short, punchy sentences and entices your audience to continue reading....",
    },

    { id:5,
      image: "/images/footer-hero-4.jpg",
      alt: "Image of boy",
      heading: "Surf's up. Winter time surfing",
      text: "Create a blog post subtitle that summarizes your post in a few short, punchy sentences and entices your audience to continue reading....",
    },
  ]
</script>

