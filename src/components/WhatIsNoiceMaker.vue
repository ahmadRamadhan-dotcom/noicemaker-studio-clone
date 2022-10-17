<template>
  <div
    class="w-full flex justify-center mt-12 sm:mt-10 md:mt-24 xl:mt-24 pb-12 sm:pb-5 md:pb-20 lg:pb-20 xl:pb-12 bg-[#1A1919]"
  >
    <div
      class="w-full sm:w-[600px] lg:w-[870px] xl:w-[88%] lg:flex lg:justify-between lg:gap-10"
    >
      <div class="sm:mt-20 xl:mt-[70px]">
        <figure v-if="!isClicked" class="relative">
          <img
            src="../assets/maxresdefault.webp"
            class="md:w-full md:h-[524px] lg:w-[500px] lg:h-[516px] xl:w-[524px] xl:h-[524px] object-cover"
            alt="a collage foto of noicer or artist in indonesia"
          />
          <button
            id="mask"
            class="absolute inset-0 grid place-content-center place-items-center xl:w-full xl:h-full"
            aria-label="this button for play video from youtube"
            @click="isClicked = !isClicked"
          >
            <img
              src="../assets/button.webp"
              class="w-16 sm:w-16 xl:w-[65px]"
              alt="play button image, this image is used for trigger iframe youtube"
            />
          </button>
          <img
            src="../assets/video-ornament.svg"
            class="absolute -bottom-4 left-5 sm:-bottom-4 sm:left-5 w-16 sm:w-20 xl:bottom-1"
            alt="tree dots of background white"
          />
        </figure>
        <IframeYoutube v-if="isClicked" />
      </div>
      <div
        class="w-[99%] lg:w-[600px] xl:w-[600px] mt-7 sm:mt-7 grid place-content-center place-items-center sm:grid sm:place-content-center sm:place-items-center xl:grid xl:place-content-center xl:place-items-center"
      >
        <span
          class="md:text-xl xl:text-xl xl:relative lg:w-full font-normal lg:flex lg:justify-between"
          >Apa itu Noicemaker Studio?
          <img
            src="../assets/star.webp"
            class="hidden sm:hidden lg:block lg:w-10 xl:w-10 xl:absolute xl:-top-10 xl:-right-1"
            alt="a picture of yellow star for waking this section beauty"
          />
        </span>
        <h2
          class="md:leading-[60px] text-center md:text-center lg:text-left xl:w-full mt-5 sm:mt-0 md:mt-5 xl:mt-5 text-3xl sm:text-[28px] md:text-5xl xl:text-5xl xl:break-words font-bold"
        >
          Selalu Ada Ruang untuk Kamu yang B<span>aru Mu</span>lai
        </h2>
        <span
          class="sm:hidden md:block text-center md:text-center lg:text-left md:text-[20px] xl:text-xl mt-4 sm:mt-0 md:mt-3 xl:mt-3"
        >
          Noicemaker Studio, membuka kesempatan bagi setiap kreator untuk
          berkembang dengan karya yang dihasilkan
        </span>
        <span class="hidden sm:block md:hidden sm:text-[16px]">
          Noicemar Studio, membuka kesempatan bagi setiap kreator untuk
          berkembang
        </span>
      </div>
    </div>
  </div>
</template>

<script>
import IframeYoutube from "./IframeYoutube.vue";
export default {
  name: "WhatIsNoiceMaker",
  data() {
    return {
      isClicked: false,
    };
  },
  components: { IframeYoutube },
};
</script>

<style scoped>
#mask {
  background: rgba(0, 0, 0, 0.5);
}

h2 span {
  background: url("../assets/banner-border.svg") bottom center;
  background-repeat: no-repeat;
}
</style>
