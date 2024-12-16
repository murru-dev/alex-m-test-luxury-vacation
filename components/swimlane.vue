<script setup lang="ts">
// Import Swiper Vue.js components
import { Swiper, SwiperSlide } from "swiper/vue";

// Import Swiper styles
import "swiper/css";

import "swiper/css/pagination";

// import "./style.css";

// import required modules
import { Pagination } from "swiper/modules";

const modules = ref([Pagination]);
</script>

<template>
  <div class="section-wrapper">
    <div class="left">
      <h1>Out of this world</h1>
      <p>
        We open the door to exceptional experiences the world over. From African
        safaris to great American road trips, our team designs epic and
        immersive Members-only itineraries.
      </p>
      <button type="button">Explore Experiences</button>
    </div>
    <div class="right">
      <swiper
        :slidesPerView="3"
        :spaceBetween="30"
        :pagination="{
          clickable: true,
        }"
        :modules="modules"
        class="mySwiper"
      >
        <swiper-slide v-for="n in 9" :key="n">
          <img src="/public/img-1.avif" style="width: 100%" />
          <h3>Some title</h3>
          <p style="width: 500px">Some text</p>
        </swiper-slide>
      </swiper>
    </div>
  </div>
</template>

<style scoped>
.section-wrapper {
  display: grid;
  grid-template-columns: auto 1fr;
}

.swiper {
  height: 100% !important;
}

.swiper-slide {
  width: 200px !important;
  /* height: 100% !important; */
}
</style>
