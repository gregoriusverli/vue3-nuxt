<template>
  <div class="bg-transparent header">
    <div class="flex flex-col lg:flex-row">
      <div
        class="flex items-center justify-between px-3 py-4 lg:py-0 border-b border-white-400 lg:border-b-0"
      >
        <div>
          <nuxt-link to="/" class="uppercase font-semibold text-white" href="#"
            >GREGORIUS</nuxt-link
          >
        </div>
        <div>
          <button
            @click.prevent="togleHeader = !togleHeader"
            class="focus:outline-none text-white block lg:hidden"
          >
            <svg
              xmlns="http://www.w3.org/2000/svg"
              class="h-6 w-6"
              fill="none"
              viewBox="0 0 24 24"
              stroke="currentColor"
            >
              <path
                stroke-linecap="round"
                stroke-linejoin="round"
                stroke-width="2"
                d="M4 6h16M4 12h16M4 18h16"
              />
            </svg>
          </button>
        </div>
      </div>

      <div
        :class="
          togleHeader
            ? 'ease-in duration-300 flex flex-col lg:flex-row justify-between w-full'
            : 'ease-out duration-300 hidden lg:flex flex-col lg:flex-row justify-between w-full'
        "
      >
        <div class="flex flex-col lg:flex-row">
          <nuxt-link
            class="block px-3 py-2 lg:py-4 text-white hover:text-black"
            to="/"
          >
            Home
          </nuxt-link>
          <nuxt-link
            class="block px-3 py-2 lg:py-4 text-white hover:text-black"
            to="/profile"
          >
            Profile
          </nuxt-link>
          <nuxt-link
            class="block px-3 py-2 lg:py-4 text-white hover:text-black"
            to="/project"
          >
            Project
          </nuxt-link>
        </div>

        <div class="flex flex-col lg:flex-row">
          <nuxt-link
            to="/journey"
            class="block px-3 py-2 lg:py-4 text-white hover:text-black"
            href="#"
            >Journey</nuxt-link
          >
          <nuxt-link
            to="/contact"
            class="block px-3 py-2 lg:py-4 text-white hover:text-black"
            href="#"
            >Contact</nuxt-link
          >
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "Header",
  data() {
    return {
      togleHeader: false,
    };
  },
};
</script>

<style>
.collapse {
  transition: 0.5s ease-out;
  background-color: blue;
}
.header {
  position: sticky !important;
  top: 0 !important;
  position: -webkit-sticky !important;
}
/* .verli {
  width: 100%;
  background-color: red;
  height: 5vh;
  text-align: center;
  align-items: center;
}

.logo {
  background-color: yellow;
  width: 15%;
  margin-left: 3%;
  vertical-align: center;
}
h1 {
  font-family: "Franklin Gothic Medium", "Arial Narrow", Arial, sans-serif;
} */
</style>
