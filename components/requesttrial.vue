<template>
  <div class="-mx-4 flex justify-center" id="requestrial">
    <div class="px-4 w-full md:w-8/12 xl:w-6/12">
      <div class="-mt-12 rounded">
        <div class="py-16 px-12">
          <div class="text-center">
            <form class="simple_form new_user">
              <div class="md:flex md:items-center mb-6">
                <div class="md:w-1/3">
                  <label
                    class="text-gray-500 font-bold md:text-center mb-1 md:mb-0 pr-2"
                    for="inline-full-name"
                  >Full name</label>
                </div>
                <div class="md:w-2/3">
                  <input
                    class="bg-gray-200 appearance-none border-2 border-gray-200 rounded w-full py-2 px-2 text-black-700 leading-tight focus:outline-none focus:bg-white focus:border-black-500"
                    type="text"
                    placeholder="John Smith"
                    v-model="fullname"
                  />
                </div>
              </div>
              <div class="md:flex md:items-center mb-6">
                <div class="md:w-1/3">
                  <label
                    class="block text-gray-500 font-bold md:text-center mb-1 md:mb-0 pr-2"
                    for="inline-username"
                  >Email</label>
                </div>
                <div class="md:w-2/3">
                  <input
                    class="bg-gray-200 appearance-none border-2 border-gray-200 rounded w-full py-2 px-2 text-gray-700 leading-tight focus:outline-none focus:bg-white focus:border-purple-500"
                    type="email"
                    placeholder="name@example.com"
                    v-model="email"
                  />
                </div>
              </div>

              <div class="md:flex md:items-center mb-6">
                <div class="md:w-1/3">
                  <label
                    class="block text-gray-500 font-bold md:text-center mb-1 md:mb-0 pr-2"
                    for="inline-username"
                  >Company</label>
                </div>
                <div class="md:w-2/3">
                  <input
                    class="bg-gray-200 appearance-none border-2 border-gray-200 rounded w-full py-2 px-4 text-gray-700 leading-tight focus:outline-none focus:bg-white focus:border-purple-500"
                    id="inline-username"
                    type="text"
                    placeholder="Company name"
                    v-model="company"
                  />
                </div>
              </div>

              <div class="md:flex md:items-center mb-6">
                <div class="md:w-1/3">
                  <label
                    class="block text-gray-500 font-bold md:text-center mb-1 md:mb-0 pr-2"
                    for="inline-username"
                  >Your role</label>
                </div>
                <div class="md:w-2/3">
                  <input
                    class="bg-gray-200 appearance-none border-2 border-gray-200 rounded w-full py-2 px-4 text-gray-700 leading-tight focus:outline-none focus:bg-white focus:border-purple-500"
                    id="inline-username"
                    type="text"
                    placeholder="What's your role in your company?"
                    v-model="role"
                  />
                </div>
              </div>

              <div class="md:flex md:items-center mb-6">
                <div class="md:w-1/3">
                  <label
                    class="block text-gray-500 font-bold md:text-center mb-1 md:mb-0 pr-2"
                    for="inline-username"
                  >Device used</label>
                </div>
                <div class="md:w-2/3">
                  <select
                    class="bg-gray-200 appearance-none border-2 border-gray-200 rounded w-full py-2 px-2 text-gray-700 leading-tight focus:outline-none focus:bg-white focus:border-blue-500"
                    v-model="selected"
                  >
                    <option disabled value class="text-gray-500">Choose your device</option>
                    <option>Walkie-Takie</option>
                    <option>Smartphones</option>
                    <option>Both</option>
                  </select>
                </div>
              </div>

              <div class="md:flex md:items-center mb-6">
                <div class="md:w-1/3">
                  <label
                    class="block text-gray-500 font-bold md:text-center mb-1 md:mb-0 pr-4"
                    for="how we can help"
                  >How we can help?</label>
                </div>
                <div class="md:w-2/3">
                  <textarea
                    class="bg-gray-200 appearance-none border-2 border-gray-200 rounded w-full py-2 px-4 text-gray-700 leading-tight focus:outline-none focus:bg-white focus:border-purple-500"
                    id="inline-username"
                    type="text"
                    placeholder="How can voiceMe.AI help you?"
                    v-model="help"
                  />
                </div>
              </div>
              <recaptcha @error="onError" @success="onSuccess" @expired="onExpired" />
              <div class="md:flex md:items-center mb-6">
                <div class="md:w-1/3"></div>
                <div class="md:w-2/3">
                  <button
                    class="shadow bg-blue-500 hover:bg-purple-400 focus:shadow-outline focus:outline-none text-white font-bold py-2 px-4 rounded"
                    type="button"
                    @click="requesttrial"
                  >Signup for a free pilot!</button>
                </div>
              </div>
            </form>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      fullname: "",
      email: "",
      company: "",
      role: "",
      selected: "",
      help: "",
      retoken: this.token
    };
  },
  methods: {
    onError(error) {
      console.log("Error happened:", error);
    },
    async requesttrial() {
      try {
        const token = await this.$recaptcha.getResponse();
        console.log("ReCaptcha token:", token);
      } catch (error) {
        console.log("Login error:", error);
      }
    },
    onSuccess(token) {
      console.log("Succeeded:", token);
    },
    onExpired() {
      console.log("Expired");
    },
    requesttrial() {
      const body = {
        fullname: this.fullname,
        email: this.email,
        company: this.company,
        role: this.role,
        selected: this.selected,
        help: this.help,
        retoken: this.retoken
      };
      this.$axios
        .$post(
          "https://api.smartear.ai/v1/contact_form",
          JSON.stringify(body),
          {
            headers: {
              "Content-Type": "application/x-www-form-urlencoded"
            }
          }
        )
        .then(function(response) {
          console.log(response);
        })
        .catch(function(error) {
          console.log(error);
        });
    }
  }
};
</script>

<style lang="scss" scoped>
</style>
