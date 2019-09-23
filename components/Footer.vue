<template>
  <!--Footer-->
  <footer class="bg-white">
    <div class="container mx-auto px-8">
      <div class="w-full flex flex-col md:flex-row py-6">
        <div class="mb-6 flex mr-4">
          <img class="h-10 fill-current inline px-2" src="~/assets/icon.png" alt="number-one" />
          <nuxt-link
            class="text-blue-600 no-underline hover:no-underline font-extrabold text-3xl lg:text-3xl"
            to="/"
          >VoiceMe.AI</nuxt-link>
        </div>

        <div class="flex-1">
          <p class="uppercase text-gray-500 md:mb-6">Links</p>
          <ul class="list-reset mb-6">
            <li class="mt-2 inline-block mr-2 md:block md:mr-0">
              <a
                href="#"
                class="no-underline hover:underline text-gray-800 hover:text-orange-500"
              >FAQ</a>
            </li>
            <li class="mt-2 inline-block mr-2 md:block md:mr-0">
              <a
                href="#"
                class="no-underline hover:underline text-gray-800 hover:text-orange-500"
              >Help</a>
            </li>
            <li class="mt-2 inline-block mr-2 md:block md:mr-0">
              <a
                href="#"
                class="no-underline hover:underline text-gray-800 hover:text-orange-500"
              >Support</a>
            </li>
          </ul>
        </div>
        <div class="flex-1">
          <p class="uppercase text-gray-500 md:mb-6">Legal</p>
          <ul class="list-reset mb-6">
            <li class="mt-2 inline-block mr-2 md:block md:mr-0">
              <a
                href="#"
                class="no-underline hover:underline text-gray-800 hover:text-orange-500"
              >Terms</a>
            </li>
            <li class="mt-2 inline-block mr-2 md:block md:mr-0">
              <a
                href="#"
                class="no-underline hover:underline text-gray-800 hover:text-orange-500"
              >Privacy</a>
            </li>
          </ul>
        </div>
        <div class="flex-1">
          <p class="uppercase text-gray-500 md:mb-6">Social</p>
          <ul class="list-reset mb-6">
            <li class="mt-2 inline-block mr-2 md:block md:mr-0">
              <a
                href="https://www.facebook.com/voiceme"
                class="no-underline hover:underline text-gray-800 hover:text-orange-500"
              >Facebook</a>
            </li>
            <li class="mt-2 inline-block mr-2 md:block md:mr-0">
              <a
                href="https://www.linkedin.com/voiceme"
                class="no-underline hover:underline text-gray-800 hover:text-blue-500"
              >Linkedin</a>
            </li>
            <li class="mt-2 inline-block mr-2 md:block md:mr-0">
              <a
                href="https://www.twitter.com/voiceme"
                class="no-underline hover:underline text-gray-800 hover:text-blue-500"
              >Twitter</a>
            </li>
          </ul>
        </div>
        <div class="flex-1">
          <p class="uppercase text-gray-500 md:mb-6">Company</p>
          <ul class="list-reset mb-6">
            <li class="mt-2 inline-block mr-2 md:block md:mr-0">
              <a
                href="#"
                class="no-underline hover:underline text-gray-800 hover:text-blue-500"
              >Official Blog</a>
            </li>
            <li class="mt-2 inline-block mr-2 md:block md:mr-0">
              <nuxt-link
                to="/about"
                class="no-underline hover:underline text-gray-800 hover:text-blue-500"
              >About Us</nuxt-link>
            </li>
            <li class="mt-2 inline-block mr-2 md:block md:mr-0">
              <nuxt-link
                to="#"
                class="no-underline hover:underline text-gray-800 hover:text-blue-500"
              >Contact</nuxt-link>
            </li>
          </ul>
        </div>
      </div>
    </div>
  </footer>
</template>

<script>
export default {};
</script>

<style lang="scss" scoped>
</style>
