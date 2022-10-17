<template>
  <div id="home" class="relative">
    <Banner />
    <WhatIsNoiceMaker />
    <WhyJoinUse />
    <img
      src="../assets/ornament-slide.svg"
      class="absolute z-[99] sm:left-32 sm:bottom-[370px] md:left-60 xl:left-40 xl:bottom-[250px]"
      alt=""
    />
    <Faqs class="absolute xl:bottom-20" />
  </div>
</template>

<script setup>
import Banner from "../components/Banner.vue";
import WhatIsNoiceMaker from "../components/WhatIsNoiceMaker.vue";
import WhyJoinUse from "../components/WhyJoinUse.vue";
import Faqs from "../components/Faqs.vue";
</script>
