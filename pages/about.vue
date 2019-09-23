<template>
  <div class="gradient">
    <Navbar />
    <header class="pt-9">
      <div class="container px-1 py-3 mx-auto flex flex-wrap flex-col md:flex-row items-center">
        <div
          class="flex flex-col w-full md:w-5/5 justify-center items-center content-center md:text-center"
        >
          <h1 class="my-4 text-5xl font-bold leading-tight text-center">About VoiceMe.AI</h1>
          <h3
            class="my-4 text-4xl font-bold leading-tight text-center"
          >Strengthen team by improving communication</h3>

          <button
            class="mx-auto lg:mx-0 hover:underline bg-white text-gray-800 font-bold rounded-full my-6 py-4 px-8 shadow-lg"
          >
            <nuxt-link to="#">Signup for a free pilot!</nuxt-link>
          </button>
        </div>
      </div>
    </header>
  </div>
</template>

<script>
import Navbar from "~/components/Navbar.vue";
export default {
  components: {
    Navbar
  }
};
</script>

<style lang="css" scoped>
.gradient {
  background: linear-gradient(90deg, #134abf 0%, #cecece 100%);
}
</style>
