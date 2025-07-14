<template>
  <section class="full-vh-section">
    <swiper
      :modules="[Navigation, Autoplay, EffectFade]"
      effect="fade"
      :fadeEffect="{ crossFade: true }"
      :autoplay="{
        delay: 5000,
        disableOnInteraction: false,
      }"
      :loop="true"
      :navigation="true"
      class="my-swiper"
    >
      <swiper-slide v-for="(slide, index) in slides" :key="index">
        <img :src="slide.img" />
        <div class="slide-text text-center">
          <div class="title">{{ slide.title }}</div>
          <div class="subtitle">{{ slide.subtitle }}</div>
        </div>
      </swiper-slide>
    </swiper>
  </section>
</template>

<script setup>
import { Swiper, SwiperSlide } from 'swiper/vue'
import 'swiper/css'
import 'swiper/css/navigation'
import 'swiper/css/autoplay'
import 'swiper/css/effect-fade'

import { Navigation, Autoplay, EffectFade } from 'swiper/modules'

const slides = [
  {
    img: 'https://preview.treethemes.com/hazel/demo2/wp-content/uploads/sites/12/revslider/IMG_0284b.jpg',
    title: 'CLEAN MINIMALIST THEME',
    subtitle:
      'The theme includes a lot of cool features, super easy to work and modify. \nFully responsive design and Visual page builder.',
  },
  {
    img: 'https://preview.treethemes.com/hazel/demo2/wp-content/uploads/sites/12/revslider/black-on-black-things-picjumbo-com.jpg',
    title: 'POWERFUL FRAMEWORK',
    subtitle:
      'The theme includes a lot of cool features, super easy to work and modify.\n Fully responsive design and Visual page builder.',
  },
]
</script>

<style>
.full-vh-section {
  height: 100vh;
}

.my-swiper {
  width: 100%;
  height: 100%;
  position: relative;
}

.my-swiper img {
  width: 100%;
  height: 100%;
  object-fit: cover;
  display: block;
}

/* 文字疊在圖片中央 */
.slide-text {
  width: 100%;
  position: absolute;
  top: 50%;
  left: 50%;
  transform: translate(-50%, -50%);
  color: white;
  font-size: 2rem;
  font-weight: bold;
  text-shadow: 0 0 8px rgba(0, 0, 0, 0.7);
  pointer-events: none;
  user-select: none;
  white-space: pre-line;
}

/* Swiper 箭頭樣式 */
.swiper-button-next,
.swiper-button-prev {
  background-color: rgba(0, 0, 0, 0.5);
  width: 48px;
  height: 48px;
  top: 50%;
  transform: translateY(-50%);
  z-index: 10;
  display: flex;
  align-items: center;
  justify-content: center;
  border-radius: 0;
  color: white;
}

.swiper-button-prev {
  left: 0;
}

.swiper-button-next {
  right: 0;
}

.swiper-button-prev::after,
.swiper-button-next::after {
  font-size: 20px;
  font-weight: bold;
}
.subtitle {
  font-family: 'Open Sans', sans-serif;
  font-size: 17px;
  font-weight: 300;
  color: rgb(221, 221, 221);
  display: block;
}
.title {
  font-family: Dosis;
  font-size: 44px;
  font-weight: 500;
  color: rgb(255, 255, 255);
  text-transform: uppercase;
  letter-spacing: 9.74138px;
  line-height: 49px;
  text-align: center;
}
</style>
