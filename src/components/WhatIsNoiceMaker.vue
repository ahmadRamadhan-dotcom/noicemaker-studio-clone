<template>
  <div
    class="w-full flex justify-center sm:mt-10 md:mt-24 xl:mt-24 sm:pb-5 xl:pb-12 bg-[#1A1919]"
  >
    <div
      class="sm:w-[550px] lg:w-[870px] xl:w-[88%] lg:flex lg:justify-between lg:gap-10"
    >
      <div class="sm:mt-20 xl:mt-[70px]">
        <figure v-if="!isClicked" class="relative">
          <img
            src="/maxresdefault.webp"
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
              src="/button.webp"
              class="sm:w-16 xl:w-[65px]"
              alt="play button image, this image is used for trigger iframe youtube"
            />
          </button>
          <img
            src="/video-ornament.svg"
            class="absolute sm:-bottom-4 sm:left-5 sm:w-20 xl:bottom-1 -left-3"
            alt="tree dots of background white"
          />
        </figure>
        <IframeYoutube v-if="isClicked" />
      </div>
      <div
        class="lg:w-[600px] xl:w-[600px] sm:mt-7 sm:grid sm:place-content-center sm:place-items-center xl:grid xl:place-content-center xl:place-items-center"
      >
        <span
          class="md:text-xl xl:text-xl xl:relative lg:w-full font-normal lg:flex lg:justify-between"
          >Apa itu Noicemaker Studio?
          <img
            src="/star.webp"
            class="sm:hidden lg:block lg:w-10 xl:w-10 xl:absolute xl:-top-10 xl:-right-1"
            alt="a picture of yellow star for waking this section beauty"
          />
        </span>
        <h2
          class="md:leading-[60px] md:text-center lg:text-left xl:w-full md:mt-5 xl:mt-5 sm:text-[28px] md:text-5xl xl:text-5xl xl:break-words font-bold"
        >
          Selalu Ada Ruang untuk Kamu yang B<span>aru Mu</span>lai
        </h2>
        <span
          class="sm:hidden md:block md:text-center lg:text-left md:text-[20px] xl:text-xl md:mt-3 xl:mt-3"
        >
          Noicemaker Studio, membuka kesempatan bagi setiap kreator untuk
          berkembang dengan karya yang dihasilkan
        </span>
        <span class="sm:block md:hidden sm:text-[16px]">
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
  background: url("/banner-border.svg") bottom center;
  background-repeat: no-repeat;
}
</style>
