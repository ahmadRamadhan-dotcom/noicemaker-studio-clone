<template>
  <div
    class="login grid place-content-center place-items-center sm:bg-[url('https://res.cloudinary.com/dk7urhntn/image/upload/v1666046828/bg-login_hqb3ix.webp')] sm:bg-[center_center] md:bg-[center_top] md:bg-[url('https://res.cloudinary.com/dk7urhntn/image/upload/v1666047437/bg-login-desktop_ocg4qm.webp')] md:mx-9 md:text-center sm:h-[120vh] md:h-[80vh] xl:h-[90vh] sm:bg-cover md:bg-contain bg-no-repeat"
  >
    <figure>
      <img
        src="../assets/noice-logo-white.svg"
        alt="a white color of noice logo"
      />
    </figure>
    <span class="sm:text-xl md:text-5xl break-words font-bold sm:mt-32 xl:mt-32"
      >Konten Audio Gratis dan Eksklusif</span
    >
    <span class="sm:text-sm md:text-xl sm:mt-10 xl:mt-10"
      >Masuk menggunakan</span
    >
    <div class="flex sm:mt-4 xl:mt-10">
      <button
        v-for="(data, index) in authIcon"
        :key="index"
        aria-label="this button for login"
        type="button"
        href="#_"
        class="inline-flex items-center justify-center px-4 py-2 text-base font-medium leading-6 text-gray-600 whitespace-no-wrap"
      >
        <img :src="data.icon" :alt="data.alt" />
      </button>
    </div>
    <span class="sm:text-[12px] md:text-xl md:mt-10 xl:mt-10"
      >Dengan mendaftar berarti kamu setuju dengan
    </span>
    <p class="sm:text-[12px] md:text-xl">
      <span class="text-[#fad810]">Syarat & Ketentuan</span>yang berlaku
    </p>
  </div>
</template>

<script setup>
const authIcon = [
  {
    id: 1,
    name: "facebook",
    alt: "nice facebook icon for login",
    icon: "https://res.cloudinary.com/dk7urhntn/image/upload/v1666049888/fb-btn_lbw3us.svg",
  },
  {
    id: 2,
    name: "google",
    alt: "fancy google icon for login",
    icon: "https://res.cloudinary.com/dk7urhntn/image/upload/v1666049888/google-btn_mayhww.svg",
  },
  {
    id: 3,
    name: "apple",
    alt: "quite nice apple icon for login",
    icon: "https://res.cloudinary.com/dk7urhntn/image/upload/v1666049888/apple-btn_xsrcun.svg",
  },
  {
    id: 4,
    name: "otp",
    alt: "a greet otp icon for login",
    icon: "https://res.cloudinary.com/dk7urhntn/image/upload/v1666049888/otp-btn_yogz4x.svg",
  },
];
</script>
