<template>
  <header
    class="w-[100%] sticky top-0 z-[999] flex justify-center sm:flex sm:justify-center bg-[#101010]"
  >
    <div
      :class="
        $route.path === '/login'
          ? ' justify-center sm:justify-center xl:grid xl:place-content-center xl:place-items-center'
          : 'justify-between sm:justify-between'
      "
      class="w-11/12 sm:w-[93%] md:w-4/5 lg:w-10/12 xl:w-[88%] 2xl:w-[1300px] flex sm:flex py-3 sm:py-3 xl:py-3"
    >
      <router-link to="/">
        <img
          :class="$route.path === '/login' ? ' xl:h-6' : 'xl:h-8'"
          src="../assets/noicemaker.svg"
          alt="noice maker header logo"
          class="h-8 sm:h-8"
        />
      </router-link>
      <router-link
        v-if="$route.path !== '/login'"
        to="/login"
        class="inline-flex tracking-[0.2em] items-center justify-center text-[0.75rem] sm:text-[0.75rem] sm:py-1 px-4 sm:px-4 xl:px-4 xl:py-1 xl:text-[0.75rem] uppercase xl:font-bold font-medium text-white whitespace-no-wrap rounded-md bg-black border border-gray-200 shadow-sm"
      >
        Masuk
      </router-link>
    </div>
  </header>
</template>
