<template>
  <div
    class="w-[500px] relative border-8 grid place-content-center place-items-center"
  >
    <img
      src="../assets/bg-circle.svg"
      alt="background image with circle"
      class="h-72"
    />
    <Swiper class="absolute z-[40] bottom-[260px]" />
  </div>
</template>

<script setup>
import Swiper from "../components/Swiper.vue";
</script>
