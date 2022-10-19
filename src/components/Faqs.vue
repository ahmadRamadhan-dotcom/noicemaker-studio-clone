<template>
  <div class="faqs flex justify-center pt-10 pb-12 sm:py-16 xl:pb-20 w-full">
    <div
      class="grid md:w-[750px] place-content-center place-items-center xl:mt-20"
    >
      <span class="md:text-xl font-normal text-[#d6d6d6]"
        >Seputar Noicemaker Studio</span
      >
      <h4
        class="text-2xl w-10/12 text-center sm:w-full sm:text-2xl md:text-[48px] md:w-11/12 md:text-center md:leading-[70px] font-bold"
      >
        Pertanyaan yang S<span>erin</span>g Muncul
      </h4>
      <Accordion class="md:mt-10" />
      <span
        class="xl:text-base xl:text-left mt-10 sm:mt-0 md:mt-10 w-11/12 sm:w-full font-bold"
        >Ada pertanyaan lain ?</span
      >
      <span class="w-11/12 sm:w-full xl:text-base font-normal"
        >Kirim email ke <span class="text-[#fad810]">creators@noice.id</span>
      </span>
    </div>
  </div>
</template>

<script>
import Accordion from "./accordion.vue";
export default {
  name: "Faqs",
  components: {
    Accordion,
  },
  data() {
    return {
      openDetail: false,
    };
  },
};
</script>

<style scoped>
.faqs {
  background-color: rgb(26, 25, 24);
}
h4 span {
  background: url("../assets/banner-border.svg") bottom center;
  background-repeat: no-repeat;
}
</style>
