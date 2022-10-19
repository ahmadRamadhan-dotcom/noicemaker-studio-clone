<template>
  <main
    id="home"
    class="relative h-[3900px] sm:h-[3180px] md:h-[3970px] xl:h-[3740px]"
  >
    <Banner />
    <WhatIsNoiceMaker />
    <WhyJoinUse />
    <img
      src="../assets/ornament-slide.svg"
      class="absolute z-[99] left-10 bottom-[1160px] sm:left-32 sm:bottom-[930px] md:bottom-[1100px] md:left-60 xl:left-40 xl:bottom-[1000px]"
      alt=""
    />
    <Faqs
      class="absolute top-[3200px] sm:top-[2600px] md:top-[3180px] xl:top-[2800px]"
    />
  </main>
</template>

<script setup>
import Banner from "../components/Banner.vue";
import WhatIsNoiceMaker from "../components/WhatIsNoiceMaker.vue";
import WhyJoinUse from "../components/WhyJoinUse.vue";
import Faqs from "../components/Faqs.vue";
</script>
