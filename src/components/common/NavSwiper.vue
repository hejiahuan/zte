<template>
  <div class="nav_swiper">
    <swiper :options="swiperOptions">
      <swiper-slide>
        <img src="https://res.vmallres.com/pimages//pages/picImages/MF5aU65jNywp0JGwznYC.jpg" alt />
      </swiper-slide>
      <swiper-slide>
        <img src="https://image.ztemall.com/d49c13361e1fe86a8165ed5230755a7c.jpg" alt />
      </swiper-slide>
      <swiper-slide>Slide 2</swiper-slide>
      <swiper-slide>Slide 3</swiper-slide>
      <swiper-slide>Slide 4</swiper-slide>
      <swiper-slide>Slide 5</swiper-slide>
      <div class="swiper-pagination" slot="pagination"></div>
    </swiper>
  </div>
</template>

<script>
import "swiper/css/swiper.css";

import { swiper, swiperSlide } from "vue-awesome-swiper";

export default {
  name: "NavSwiper",
  data() {
    return {
      swiperOptions: {
        pagination: {
          el: ".swiper-pagination"
        },
        autoplay: true
      }
    };
  },
  components: {
    swiper,
    swiperSlide
  }
};
</script>

<style lang="scss" scoped>
.nav_swiper {
  margin-top: 6px;
  .swiper-container {
    height: 510px;
    .swiper-slide {
      img {
        width: 100%;
        height: 100%;
      }
    }
  }
}
</style>