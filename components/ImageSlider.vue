<template>
<vueper-slides 
  slide-image-inside
  :visible-slides="2"
  slide-multiple
  :slide-ratio="1/4"
  :gap="2"
  :dragging-distance="200"
  :bullets="false"
  :arrows-outside="false"
  >
  <vueper-slide 
    class="no-shadow thumbnails"
    v-for="(slide, i) in slides"
    v-bind:key="i"
    v-bind:logo="slide.logo"
    v-bind:image="slide.image"
    v-bind:title="slide.title"
    v-bind:content="slide.content"
  >
  </vueper-slide>
</vueper-slides>
</template>

<script setup>
  import { VueperSlides, VueperSlide } from 'vueperslides'
  import 'vueperslides/dist/vueperslides.css'
  const slides = [
    {
      logo: 'LibreMedia',
      title: 'Season 2 Episode 1',
      content: 'excerpt of episode 1',
      image: 'assets/images/A-la-bonne-franquette/S2-E1.png'
    },
    {
      logo: 'LibreMedia',
      title: 'Season 2 Episode 2',
      content: 'excerpt of episode 2',
      image: 'assets/images/A-la-bonne-franquette/S2-E2.png'
    },
    {
      logo: 'LibreMedia',
      title: 'Season 2 Episode 3',
      content: 'excerpt of episode 3',
      image: 'assets/images/A-la-bonne-franquette/S2-E3.png'
    }
  ]
</script>

<style>
.vueperslide {
  background: linear-gradient(-45deg, #ee7752, #e73c7e, #23a6d5, #23d5ab);
}

.vueperslide__title {
  font-size: 2em; 
  opacity: 0.7; 
  color: white; 
}

.vueperslide__logo {
  font-size: 3em; 
}

p {
  position: absolute;
  top: 5px;
  right: 5px;
  z-index: 10;
}



</style>
