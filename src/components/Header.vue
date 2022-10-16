<template>
  <div
    class="w-full sticky top-0 z-[30] flex justify-center sm:flex sm:justify-center bg-[#101010]"
  >
    <div
      class="w-11/12 sm:w-[93%] md:w-4/5 lg:w-10/12 xl:w-[88%] flex justify-between sm:flex sm:justify-between py-3 sm:py-3 xl:py-3"
    >
      <router-link to="/">
        <img
          src="/noicemaker.svg"
          alt="noice maker header logo"
          class="h-8 sm:h-8 xl:h-8"
        />
      </router-link>
      <router-link
        to="/login"
        class="inline-flex tracking-[0.2em] items-center justify-center text-[0.75rem] sm:text-[0.75rem] sm:py-1 px-4 sm:px-4 xl:px-4 xl:py-1 xl:text-[0.75rem] uppercase xl:font-bold font-medium text-white whitespace-no-wrap rounded-md bg-black border border-gray-200 shadow-sm"
      >
        Masuk
      </router-link>
    </div>
  </div>
</template>
