<template>
  <swiper class="mySwiper" :parallax="true">
    <swiper-slide
      v-for="image in images"
      :key="image.id"
      class="justify-center"
    >
      <div class="container block">
        <div class="imageandgrad">
          <img :src="image.imageurl" class="background" />
          <div class="gradient"></div>
          <div class="shadowoverlay"></div>
        </div>
        <div class="overlaytext">
          <img
            class="logo"
            src="https://libremedia.ca/img/logo-wh ite-large.png"
          />
          <h1 class="title">{{ image.title }}</h1>
          <p class="saison">{{ image.saison }}</p>
          <p class="episode">{{ image.episode }}</p>
        </div>
        <img href="#" class="playbutton" src="~assets/play-icon.svg"/>
        <div class="text-right">
          Lorem ipsum dolor sit amet, consectetur adipiscing elit. Nullam ornare
          nisi ut odio rutrum egestas. Etiam eleifend, nisl non sodales
          ultrices, lorem ante aliquam velit, quis imperdiet nunc purus non
          velit. Nam est turpis, semper et rutrum nec, sagittis feugiat turpis.
          Sed egestas dolor eu eros consectetur molestie. Donec laoreet, odio
          vel accumsan tempus, lorem sapien iaculis neque, et pretium tellus sem
          eu diam. Sed vitae dapibus felis. In molestie dolor eget rutrum
          volutpat. Curabitur egestas mauris in leo posuere, in consectetur
          purus commodo.
        </div>
      </div>
    </swiper-slide>
  </swiper>
</template>

<script setup>
import { Swiper, SwiperSlide } from "swiper/vue";
import "swiper/css";

import image1 from "assets/images/A-la-bonne-franquette/S2-E1.png";
import image2 from "assets/images/A-la-bonne-franquette/S2-E2.png";
import image3 from "assets/images/A-la-bonne-franquette/S2-E3.png";

const images = [
  {
    id: 1,
    imageurl: image1,
    title: "À la bonne franquette!",
    saison: "Saison 2",
    episode: "Épisode 1",
  },
  {
    id: 2,
    imageurl: image2,
    title: "À la bonne franquette!",
    saison: "Saison 2",
    episode: "Épisode 2",
  },
  {
    id: 3,
    imageurl: image3,
    title: "À la bonne franquette!",
    saison: "Saison 2",
    episode: "Épisode 3",
  },
  {
    id: 4, 
    imageurl: image2, 
    title: "À la bonne franquette!",
    saison: "Saison 2",
    episode: "Épisode 4",
  }
];
</script>

<style>
.container .text-right {
  color: white;
  position: absolute;
  left: 62%;
  top: 5%;
  text-align: left; 
  font-family: 'metropolis-bold';
}
* {
  box-sizing: border-box;
}

.container {
  margin: 10px 10px 10px 10px;
}

.container .background {
  position: relative;
  z-index: 0;
  border-radius: 15px 15px 15px 15px;
}

.container .shadowoverlay {
  box-shadow: inset 0px 0px 10px 5px #1f2937;
  z-index: 2;
  height: 98%;
  width: 60%;
  position: absolute;
  left: 10px;
  top: 10px;
  margin-bottom: 10px;
  border-radius: 15px 15px 15px 15px;
}
.container .imageandgrad {
  width: 100%;
}

.container .gradient {
  position: absolute;
  background: linear-gradient(
    to top left,
    rgba(0, 0, 0, 0) 50%,
    rgba(0, 0, 0, 0.9) 100%
  );
  top: 0%;
  left: 0%;
  width: 1000px;
  height: 800px;
  margin: 10px 10px 10px 10px;
}

.container .overlaytext {
  position: absolute;
  left: 2%;
  top: 4%;
}
.container .logo {
  height: 3em;
}

.container .title {
  font-size: 60px;
  font-family: "metropolis-bold";
  font-weight: 600;
  line-height: 1;
  text-transform: uppercase;
  color: white;
  box-sizing: border-box;
  width: 350px;
  padding-bottom: 10px;
  padding-top: 12px;
}

.container .saison {
  font-size: 25px;
  color: white;
  font-family: "metropolis-bold";
  font-weight: 400;
}

.container .episode {
  font-size: 35px;
  color: white;
  font-family: "metropolis-bold";
  font-weight: 300;
}

.container .playbutton {
  position: absolute; 
  left: 25%;
  top: 35%;
  width: 200px;
  
}
</style>
