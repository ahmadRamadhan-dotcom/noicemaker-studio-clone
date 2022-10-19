<template>
  <div class="w-full flex justify-center mt-12 sm:mt-10 xl:mt-8 2xl:mt-10">
    <div class="grid relative text-center">
      <span class="sm:text-base md:text-xl">
        Kenapa Gabung Noicemaker Studio
      </span>
      <h3
        class="text-[28px] sm:text-[28px] lg:text-5xl font-bold lg:mt-5 xl:mt-6"
      >
        Buat se<span>sukan</span>ya, Atur semaunya
      </h3>
      <span class="lg:text-xl lg:mt-5 xl:mt-4"
        >Jadikan karyamu lebih bermakna bersama Noice
      </span>
      <CardJoinUs :noiceData="noiceData" />
      <Swiper
        class="absolute -top-[320%] sm:bottom-[330px] sm:-top-[380px] lg:bottom-[390px] lg:-left-32 xl:bottom-[272px] xl:-top-[270px] xl:-left-80"
      />
    </div>
  </div>
</template>

<script setup>
import CardJoinUs from "./CardJoinUs.vue";
import Swiper from "./Swiper.vue";

const noiceData = [
  {
    id: 1,
    title: "Berkarya dengan data",
    content:
      "Maksimalkan performa konten dengan analitik yang di update setiap hari",
    image: "statistics-asset.svg",
    alt: "image of statistic play or listener in noice",
    arrow: "ornament-right",
  },
  {
    id: 2,
    title: "Interaksi langsung dengan pendengarmu",
    content:
      "Cari tau apa yang ada di pikiran pendengar dengan ngobrol langsung lewat Noice Live. Pssst 2000 orang bisa join secara bersamaan lho.",
    image: "mobile-app-landing.svg",
    alt: "an image of noice live in noice application",
    arrow: "ornament-left",
  },
  {
    id: 3,
    title: "Dukungan penuh untuk Noicemaker",
    content:
      "Dukungan edukasi, produksi, hingga promosi disiapkan untuk Noicemaker yang ingin berkembang bersama Noice. Pastikan kamu salah satunya.",
    image: "",
    alt: "",
    arrow: "",
  },
];
</script>

<style scoped>
h3 span {
  background: url("../assets/banner-border.svg") bottom center;
  background-repeat: no-repeat;
}
</style>
