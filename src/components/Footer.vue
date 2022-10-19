<template>
  <footer class="flex justify-center md:pb-14 xl:pb-14">
    <div
      class="sm:w-[600px] md:w-[650px] lg:w-[850px] xl:w-[1200px] md:flex md:justify-between"
    >
      <div
        class="sm:flex sm:flex-col-reverse md:flex md:flex-row xl:flex md:gap-[90px] xl:gap-[100px]"
      >
        <div class="sm:hidden md:block">
          <figure>
            <img
              src="../assets/noice-logo-full.svg"
              alt="full logo of noice.id"
            />
          </figure>
          <div class="md:mt-10 xl:mt-7 flex gap-4">
            <a
              href="https://play.google.com/store/apps/details?id=noice.app"
              target="_blank"
              title="Google Play"
            >
              <img
                src="../assets/google-play-icon.svg"
                class="md:h-6 h-8"
                alt="google play icon"
              />
            </a>
            <a
              href="https://apps.apple.com/us/app/noice-radio-music-podcast/id1484372791?ls=1"
              target="_blank"
              title="App Store"
            >
              <img
                src="../assets/appstore-icon.svg"
                class="md:h-6 h-8"
                alt="appstore icon"
              />
            </a>
          </div>
          <p class="md:mt-16 xl:mt-16">© Noice 2022</p>
        </div>
        <ul class="text-base md:leading-[50px] xl:leading-[35px]">
          <li class="font-bold">Aturan yang berlaku</li>
          <li>Ketentuan Konten</li>
          <li>Syarat & Ketentuan</li>
          <li>Kebijakan Privasi</li>
        </ul>
      </div>
      <div class="sm:mt-3 xl:w-60">
        <span class="font-bold">Ikuti Kami</span>
        <div class="sm:flex xl:flex gap-4">
          <a
            v-for="(data, index) in noiceSocialMedia"
            :key="index"
            target="_blank"
            class="mt-5 cursor-pointer text-center text-black w-8 h-8 sm:w-7 sm:h-7 lg:w-8 lg:h-8 rounded-full grid place-content-center place-items-center items-center"
          >
            <img :src="data.icon" :alt="data.name + 'icon'" />
          </a>
        </div>
      </div>
      <div class="sm:mt-20 md:hidden">
        <figure>
          <img
            src="../assets/noice-logo-full.svg"
            alt="full logo of noice.id"
          />
        </figure>
        <div class="sm:mt-7 flex gap-4">
          <a
            href="https://play.google.com/store/apps/details?id=noice.app"
            target="_blank"
            title="Google Play"
          >
            <img
              src="../assets/google-play-icon.svg"
              class="h-8"
              alt="google play icon"
            />
          </a>
          <a
            href="https://apps.apple.com/us/app/noice-radio-music-podcast/id1484372791?ls=1"
            target="_blank"
            title="App Store"
          >
            <img
              src="../assets/appstore-icon.svg"
              class="h-8"
              alt="appstore icon"
            />
          </a>
        </div>
        <p class="sm:text-center sm:mt-16">© Noice 2022</p>
      </div>
    </div>
  </footer>
</template>
<script setup>
const noiceSocialMedia = [
  {
    id: 1,
    name: "instagram",
    href: "https://www.instagram.com/noice.id/",
    icon: "https://res.cloudinary.com/dk7urhntn/image/upload/v1666137309/instagram_ubqhni.svg",
  },
  {
    id: 2,
    name: "facebook",
    href: "https://www.facebook.com/noice.id",
    icon: "https://res.cloudinary.com/dk7urhntn/image/upload/v1666137309/facebook_ahasvv.svg",
  },
  {
    id: 3,
    name: "youtube",
    href: "https://www.youtube.com/c/NOICEYouTube",
    icon: "https://res.cloudinary.com/dk7urhntn/image/upload/v1666137425/youtube_rpq4xl.svg",
  },
  {
    id: 4,
    name: "twitter",
    href: "https://twitter.com/noice_id",
    icon: "https://res.cloudinary.com/dk7urhntn/image/upload/v1666137309/twitter_akqayy.svg",
  },
  {
    id: 5,
    name: "tiktok",
    href: "https://tiktok.com/@noice.id",
    icon: "https://res.cloudinary.com/dk7urhntn/image/upload/v1666137309/tik_tok_dogxph.svg",
  },
];
</script>
<style lang=""></style>
