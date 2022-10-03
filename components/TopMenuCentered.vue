<template>
  <div class="sticky top-16 z-20 bg-gray-800 text-white sm:top-10">
    <div class="mx-auto px-4 sm:px-10">
      <div
        class="flex items-center justify-between py-6 md:justify-start md:space-x-10"
      >
        <div class="flex justify-start lg:w-0 lg:flex-1">
          <button
            type="button"
            @click="menuOpen = !menuOpen"
            class="rounded-lg border-2 border-white bg-transparent py-2 px-2 text-cyan-600 hover:bg-white"
          >
            <span class="sr-only">Open Menu</span>
            <!--
            Icon when menu is closed
            Menu open: "hidden", Menu closed: "block"
            -->
            <img class="m-auto h-9 w-fit" src="~assets/menu-icon.svg" />
          </button>
          <NuxtLink to="/" class="flex justify-center">
            <img
              class="sm:m-left m-auto ml-4 h-9 w-fit justify-center sm:w-64"
              src="https://libremedia.ca/img/logo-white-large.png"
            />
          </NuxtLink>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      menuOpen: false,
    };
  },
};
</script>
