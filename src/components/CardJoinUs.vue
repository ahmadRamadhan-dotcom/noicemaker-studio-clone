<template>
  <div
    v-for="(data, index) in noiceData"
    :key="index"
    :class="{
      'lg:flex-row-reverse': data.id === 2,
    }"
    class="w-11/12 sm:w-[600px] lg:w-[700px] mb-20 sm:mb-0 xl:w-[1000px] relative mt-24 sm:mt-16 xl:mt-16 mx-auto sm:mx-0 sm:grid sm:place-content-center sm:place-items-center lg:flex lg:justify-between xl:flex xl:justify-between xl:items-center"
  >
    <figure v-if="data.id !== 3">
      <img
        class="lg:w-[500px] mx-auto sm:mx-0 xl:w-[350px]"
        :src="'/' + data.image"
        alt="image of statistic user in noice"
      />
    </figure>

    <img
      v-if="data.id === 3"
      src="../assets/bg-circle.svg"
      alt="background image with circle"
      class="h-72 mx-auto sm:mx-0 xl:mt-20 w-[200px] sm:w-[225px] lg:w-[800px] xl:w-[350px]"
    />
    <div
      :class="data.id === 3 ? 'xl:mt-20' : ''"
      class="lg:w-[500px] xl:w-[540px] relative xl:text-left grid sm:grid xl:grid"
    >
      <span
        class="text-2xl mt-10 sm:mt-0 sm:text-2xl lg:text-[40px] xl:text-[40px] font-bold lg:text-left lg:leading-[60px] lg:w-[200px] xl:w-full"
        >{{ data.title }}</span
      >
      <span class="lg:text-xl lg:w-[200px] xl:w-full lg:text-left xl:mt-4">{{
        data.content
      }}</span>
      <button
        aria-label="button for more information"
        v-if="data.id === 3"
        class="inline-flex items-center justify-center mb-3 mr-1 text-[12px] py-2 sm:py-3 sm:mx-auto md:mx-auto lg:mx-0 xl:py-3.5 sm:mt-4 xl:mt-3 rounded-sm font-bold text-black no-underline align-middle uppercase bg-white sm:w-48 xl:w-[170px] tracking-[0.2em] sm:tracking-[0.2em] xl:tracking-[0.2em]"
      >
        Selengkapnya
        <svg
          class="w-4 h-4 ml-2"
          fill="none"
          stroke="currentColor"
          viewBox="0 0 24 24"
          xmlns="http://www.w3.org/2000/svg"
        >
          <path
            stroke-linecap="round"
            stroke-linejoin="round"
            stroke-width="2"
            d="M14 5l7 7m0 0l-7 7m7-7H3"
          ></path>
        </svg>
      </button>

      <figure>
        <img
          :src="'/' + data.arrow + '.svg'"
          :alt="data.alt"
          :class="
            data.id === 1
              ? 'right-10 top-52 sm:right-10 sm:top-20 lg:top-80 lg:w-32 xl:top-52 xl:left-32'
              : 'left-1 top-72 sm:top-20 xl:bottom-32 xl:top-72 xl:left-32 '
          "
          class="xl:w-24 absolute"
        />
      </figure>
    </div>
  </div>
</template>

<script setup>
import Swiper from "./Swiper.vue";

const props = defineProps({
  noiceData: Array,
});
</script>
