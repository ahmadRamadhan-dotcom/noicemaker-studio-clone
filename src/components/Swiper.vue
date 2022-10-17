<template>
  <swiper
    :pagination="{
      clickable: true,
    }"
    :modules="modules"
    class="mySwiper max-w-[250px] sm:max-w-[261px] lg:max-w-[350px] xl:max-w-[361px] cursor-pointer"
  >
    <swiper-slide v-for="(data, index) in noiceData" :key="index">
      <img :src="data.image" alt="" />
    </swiper-slide>
  </swiper>
</template>
<script>
// Import Swiper Vue.js components
import { Swiper, SwiperSlide } from "swiper/vue";

// Import Swiper styles
import "swiper/css";

import "swiper/css/pagination";

// import required modules
import { Pagination } from "swiper";

export default {
  data() {
    return {
      noiceData: [
        {
          id: 1,
          image:
            "https://res.cloudinary.com/dk7urhntn/image/upload/v1665980850/podcast-slide-one_istewt.webp",
        },
        {
          id: 2,
          image:
            "https://res.cloudinary.com/dk7urhntn/image/upload/v1665980850/podcast-slide-two_ud3km7.webp",
        },
        {
          id: 3,
          image:
            "https://res.cloudinary.com/dk7urhntn/image/upload/v1665980850/podcast-slide-three_p1aatw.webp",
        },
        {
          id: 4,
          image:
            "https://res.cloudinary.com/dk7urhntn/image/upload/v1665980850/podcast-slide-four_scuylb.webp",
        },
      ],
    };
  },
  components: {
    Swiper,
    SwiperSlide,
  },
  setup() {
    return {
      modules: [Pagination],
    };
  },
};
</script>

<style scoped>
.swiper-slide {
  text-align: center;
  font-size: 18px;
  color: black;
  /* background: #fff; */

  /* Center slide text vertically */
  display: -webkit-box;
  display: -ms-flexbox;
  display: -webkit-flex;
  display: flex;
  -webkit-box-pack: center;
  -ms-flex-pack: center;
  -webkit-justify-content: center;
  justify-content: center;
  -webkit-box-align: center;
  -ms-flex-align: center;
  -webkit-align-items: center;
  align-items: center;
}

.swiper-slide img {
  display: block;
  width: 100%;
  height: 100%;
  object-fit: cover;
}
</style>
