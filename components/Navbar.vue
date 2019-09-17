<template>
  <nav id="header" class="w-full z-30 text-white">
    <div class="w-full container mx-auto flex flex-wrap items-center justify-between mt-0 py-2">
      <div class="pl-4 flex items-center">
        <img class="h-8 fill-current inline" src="~/assets/number-one.png" alt="number-one" />

        <nuxt-link
          class="toggleColour text-white no-underline hover:no-underline font-bold text-2xl lg:text-4xl"
          to="/"
        >VoiceMe.ai</nuxt-link>
      </div>

      <div
        class="w-full flex-grow lg:flex lg:items-center lg:w-auto hidden lg:block mt-2 lg:mt-0 bg-white lg:bg-transparent text-black p-4 lg:p-0 z-20"
        id="nav-content"
      >
        <ul class="list-reset lg:flex justify-end flex-1 items-center">
          <li class="mr-3">
            <nuxt-link
              class="inline-block py-2 px-4 text-black font-bold no-underline"
              to="/dashboard"
            >Dashboard</nuxt-link>
          </li>
          <li class="mr-3">
            <nuxt-link
              class="inline-block text-black no-underline font-bold hover:text-gray-800 hover:text-underline py-2 px-4"
              to="about"
            >About Us</nuxt-link>
          </li>
        </ul>
      </div>
    </div>

    <hr class="border-b border-gray-100 opacity-25 my-0 py-0" />
  </nav>
</template>

<script>
export default {};
</script>

<style lang="scss" scoped>
</style>
