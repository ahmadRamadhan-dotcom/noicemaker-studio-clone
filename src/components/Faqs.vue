<template>
  <div class="faqs flex justify-center w-full">
    <div class="grid place-content-center place-items-center xl:mt-20">
      <span class="xl:text-xl font-normal text-[#d6d6d6]"
        >Seputar Noicemaker Studio</span
      >
      <h4 class="xl:text-[48px] font-bold">
        Pertanyaan yang S<span>erin</span>g Muncul
      </h4>
    </div>
  </div>
</template>

<script>
export default {
  name: "Faqs",
  components: {},
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
