<template>
  <div class="gradient font-body">
    <nav id="header" class="w-full z-30 text-white">
      <div class="w-full container mx-auto flex flex-wrap items-center justify-between mt-0 py-2">
        <div class="pl-4 flex items-center">
          <img class="h-10 fill-current inline px-2" src="~/assets/icon.png" alt="number-one" />

          <nuxt-link
            class="toggleColour text-white no-underline hover:no-underline font-bold text-2xl lg:text-4xl"
            to="/"
          >VoiceMe.AI</nuxt-link>
        </div>
        <div class="block sm:hidden">
          <button
            @click="toggle"
            class="flex items-center px-3 py-2 border rounded text-teal-lighter border-teal-light hover:text-white hover:border-white"
          >
            <svg
              class="fill-current h-3 w-3"
              viewBox="0 0 20 20"
              xmlns="http://www.w3.org/2000/svg"
            >
              <title>Menu</title>
              <path d="M0 3h20v2H0V3zm0 6h20v2H0V9zm0 6h20v2H0v-2z" />
            </svg>
          </button>
        </div>

        <div
          :class="open ? 'block': 'hidden'"
          class="w-full flex-grow sm:flex sm:items-center sm:w-auto"
        >
          <div class="text-sm sm:flex-grow">
            <nuxt-link
              class="block py-2 px-4 lg:invisible text-white sm:inline-block font-bolder text-lg no-underline mt-4"
              to="/"
            >Home</nuxt-link>
            <nuxt-link
              class="block py-2 px-4 lg:invisible text-white sm:inline-block font-bolder text-lg no-underline mt-4"
              to="/dashboard"
            >Dashboard</nuxt-link>
            <nuxt-link
              class="block py-2 px-4 lg:invisible text-white sm:inline-block font-bolder text-lg no-underline mt-4"
              to="/about"
            >About us</nuxt-link>
          </div>
        </div>
        <div
          class="w-full flex-grow lg:flex lg:items-center lg:w-auto hidden lg:block mt-2 lg:mt-0 bg-white lg:bg-transparent text-black p-4 lg:p-0 z-20"
          id="nav-content"
        >
          <ul class="list-reset lg:flex justify-end flex-1 items-center">
            <li class="mr-3">
              <nuxt-link
                class="inline-block py-2 px-4 text-white font-bold no-underline hide-me"
                to="/"
              >Home</nuxt-link>
            </li>
            <li class="mr-3">
              <nuxt-link
                class="inline-block py-2 px-4 text-white font-bold no-underline"
                to="/dashboard"
              >Dashboard</nuxt-link>
            </li>
            <li class="mr-3">
              <nuxt-link
                class="inline-block text-white no-underline font-bold hover:text-gray-800 hover:text-underline py-2 px-4"
                to="about"
              >About Us</nuxt-link>
            </li>
          </ul>
        </div>
      </div>

      <hr class="border-b border-gray-100 opacity-25 my-0 py-0" />
    </nav>
    <div class="container mx-auto px-4 gradient">
      <div class="flex flex-wrap -mx-4 my-5">
        <!--Left Col-->
        <div class="w-full lg:w-2/5 px-4 text-center lg:text-left self-center">
          <h1 class="mb-8 text-5xl font-bold leading-none text-white">About Us</h1>
          <p
            class="mb-6 text-white text-xl"
          >Our solution is a simple way to bridge the gap between analog and digital technology. People who are familiar with walkie-talkies and CB radios don't have to change their behavior, and managers get the added benefit of using a visual dashboard to help them stay connected to their team's communication.</p>

          <button
            class="mx-auto lg:mx-0 hover:underline bg-white text-gray-800 font-bold rounded-full my-6 py-4 px-8 shadow-lg"
            v-scroll-to="'#requestrial'"
          >Sign up for a free pilot!</button>
        </div>
        <!--Right Col-->
        <div class="w-full lg:w-3/5 px-4 text-center lg:text-right lg:text-left self-end px-4">
          <img class="w-full xl:w-4/5 z-50 inline-block" src="~/assets/team.svg" />
        </div>
      </div>
    </div>
    <div class="relative -mt-12 lg:-mt-24">
      <svg
        viewBox="0 0 1428 174"
        version="1.1"
        xmlns="http://www.w3.org/2000/svg"
        xmlns:xlink="http://www.w3.org/1999/xlink"
      >
        <g stroke="none" stroke-width="1" fill="none" fill-rule="evenodd">
          <g transform="translate(-2.000000, 44.000000)" fill="#FFFFFF" fill-rule="nonzero">
            <path
              d="M0,0 C90.7283404,0.927527913 147.912752,27.187927 291.910178,59.9119003 C387.908462,81.7278826 543.605069,89.334785 759,82.7326078 C469.336065,156.254352 216.336065,153.6679 0,74.9732496"
              opacity="0.100000001"
            />
            <path
              d="M100,104.708498 C277.413333,72.2345949 426.147877,52.5246657 546.203633,45.5787101 C666.259389,38.6327546 810.524845,41.7979068 979,55.0741668 C931.069965,56.122511 810.303266,74.8455141 616.699903,111.243176 C423.096539,147.640838 250.863238,145.462612 100,104.708498 Z"
              opacity="0.100000001"
            />
            <path
              d="M1046,51.6521276 C1130.83045,29.328812 1279.08318,17.607883 1439,40.1656806 L1439,120 C1271.17211,77.9435312 1140.17211,55.1609071 1046,51.6521276 Z"
              id="Path-4"
              opacity="0.200000003"
            />
          </g>
          <g transform="translate(-4.000000, 76.000000)" fill="#FFFFFF" fill-rule="nonzero">
            <path
              d="M0.457,34.035 C57.086,53.198 98.208,65.809 123.822,71.865 C181.454,85.495 234.295,90.29 272.033,93.459 C311.355,96.759 396.635,95.801 461.025,91.663 C486.76,90.01 518.727,86.372 556.926,80.752 C595.747,74.596 622.372,70.008 636.799,66.991 C663.913,61.324 712.501,49.503 727.605,46.128 C780.47,34.317 818.839,22.532 856.324,15.904 C922.689,4.169 955.676,2.522 1011.185,0.432 C1060.705,1.477 1097.39,3.129 1121.236,5.387 C1161.703,9.219 1208.621,17.821 1235.4,22.304 C1285.855,30.748 1354.351,47.432 1440.886,72.354 L1441.191,104.352 L1.121,104.031 L0.457,34.035 Z"
            />
          </g>
        </g>
      </svg>
    </div>
    <section class="bg-white border-b py-8">
      <a class="container mx-auto flex flex-wrap pt-4 pb-12">
        <p class="w-full my-2 text-2xl font-bold text-center text-gray-800">Our Story</p>
        <div class="w-full mb-4">
          <div class="h-1 mx-auto gradient w-64 opacity-20 my-0 py-0 rounded-t"></div>
          <p
            class="w-full my-2 text-1xl text-center text-gray-800 px-8"
          >We started VoiceMe.AI to help people who are techno-phobic make the leap into a digital world. Almost all communication today is digital, and for millions of workers across the country, utilizing advanced technology can be challenging.</p>
        </div>
      </a>
    </section>

    <section class="bg-white border-b py-8">
      <div class="container max-w-5xl mx-auto m-8">
        <div class="w-full mb-4">
          <div class="h-1 mx-auto gradient w-64 opacity-25 my-0 py-0 rounded-t"></div>
        </div>
        <div class="flex flex-wrap">
          <div class="w-5/6 sm:w-1/2 p-6">
            <h3 class="text-3xl text-gray-800 font-bold leading-none mb-3">Our Mission</h3>
            <p class="text-black-600 mb-8">
              Our mission is to strengthen teams in Service Industries like hospitality, security,
              construction, healthcare, and transportation by improving the way people
              communicate on a daily basis. When teams communicate well,
              they work efficiently because they are better informed
              and more confident in their actions. This not only improves customer service,
              it improves their working condition and potentially their lives.
              <br />
            </p>
          </div>
          <div class="w-full sm:w-1/2 p-6">
            <svg
              class="w-full sm:h-64 mx-auto"
              version="1.1"
              xmlns="http://www.w3.org/2000/svg"
              xmlns:xlink="http://www.w3.org/1999/xlink"
              x="0px"
              y="0px"
              viewBox="0 0 1000 1000"
              style="enable-background:new 0 0 1000 1000;"
              xml:space="preserve"
            >
              <style type="text/css">
  .st0 {
    fill: #f3f3f3;
  }
  .st1 {
    fill: #e1e1e1;
  }
  .st2 {
    fill: #fd8369;
  }
  .st3 {
    fill: #ffffff;
  }
  .st4 {
    fill: #de8e68;
  }
  .st5 {
    fill: #6fc9ce;
  }
  .st6 {
    fill: #febf92;
  }
  .st7 {
    fill: #fed892;
  }
  .st8 {
    fill: none;
    stroke: #000000;
    stroke-width: 0.95;
    stroke-miterlimit: 10;
  }
  .st9 {
    fill: none;
    stroke: #000000;
    stroke-width: 1.0746;
    stroke-linecap: round;
    stroke-miterlimit: 10;
  }
  .st10 {
    fill: #74d5de;
  }
  .st11 {
    fill: #fecc92;
  }
  .st12 {
    fill: #d38466;
  }
              </style>
              <g id="Background">
                <rect x="109.9" y="43" class="st0" width="727.7" height="717.3" />
                <rect x="109.9" y="43" class="st1" width="727.7" height="54.6" />
                <circle class="st2" cx="148.3" cy="71" r="8.6" />
                <circle class="st2" cx="176" cy="71" r="8.6" />
                <circle class="st2" cx="203.7" cy="71" r="8.6" />
                <rect x="145.5" y="137.4" class="st3" width="290.9" height="157.6" />
                <rect x="145.5" y="332.4" class="st3" width="290.9" height="157.6" />
                <rect x="507.2" y="332.4" class="st3" width="290.9" height="339.9" />
                <rect x="486.9" y="148.8" class="st1" width="399.4" height="15.2" />
                <rect x="486.9" y="191.7" class="st1" width="399.4" height="15.2" />
                <rect x="486.9" y="234.6" class="st1" width="399.4" height="15.2" />
                <rect x="486.9" y="277.5" class="st1" width="399.4" height="15.2" />
              </g>
              <g id="Foreground">
                <rect x="689.9" y="756.2" class="st4" width="15.3" height="23.2" />
                <rect x="870.2" y="854.2" class="st4" width="15.3" height="23.2" />
                <path
                  class="st5"
                  d="M802.2,541.5c-18.5,0-101.1,82.1-108.3,95.9c-7.2,13.8-5.1,121.9-5.1,121.9l17.8,3.4L735.5,662
		c12.6-1.5,65.6-12.9,93-35c27.4-22.2-2.6-71.7-2.6-71.7L802.2,541.5z"
                />
                <path
                  class="st4"
                  d="M771.3,430c-9.1,8.1-27.3,28.4-28.8,31c-4.6-2.2-52.5-27.4-56.1-29c-3.6-1.6-11.2-14.3-13.8-14.3
		c-1.5,0-2.9,2.9-2.9,4.9c0,3.4,1.6,6,2.6,7.1c-3.4-0.5-33.4-2.8-33.4-0.8c0,5.2,33.6,12.1,36.2,13.5c2.6,1.4,57.3,52,76.3,52
		c7.4,0,40.1-22.2,40.1-24.6c3.1-2.1,7.9-5.2,7.9-5.2v-17.6l-11.4-8.3C788,438.6,773.1,428.4,771.3,430z"
                />
                <path
                  class="st6"
                  d="M770.1,424.2c2-16.2,39.3-53,56.4-36.6c14.9,14.3-12.1,65.4-19,67.4C799.7,455.8,769.6,435.2,770.1,424.2z"
                />
                <path
                  class="st7"
                  d="M883.9,390.5c19-8,45.6,36,42.6,52c0,7-39,22-45,18S864.9,398.5,883.9,390.5z"
                />
                <path class="st8" d="M801.7,449.6" />
                <path class="st9" d="M854.7,340.5" />
                <path
                  class="st10"
                  d="M807.3,548.6l62.8,305.5h16.1l5.7-272.5c0-4.7-0.4-34.3-0.4-38.1C873.3,548.8,834.5,553,807.3,548.6z"
                />
                <polygon points="870.2,877.4 885.5,877.4 885.5,894 843.3,894 	" />
                <polygon points="689.9,779.4 705.2,779.4 705.2,796 663,796 	" />
                <rect x="598" y="796" class="st2" width="182.1" height="106.6" />
                <polygon class="st2" points="140.7,908.4 70.4,907.6 45.8,817.3 163.7,817.3 	" />
                <path
                  class="st11"
                  d="M842.3,367c47,0,63.4,39.1,63.4,51.8c0,12.7-14.7,90.2-14.1,124.7c0.1,5.7-84.3,10.8-95.8,2.5
		C790.4,542.1,778.8,367,842.3,367z"
                />
                <path
                  class="st4"
                  d="M926.5,442.5c13.3,20.4,12.5,67.4,12.5,74.5c0,7.1-49.6,70.9-53.9,70.9c-2.6-2.6-9.8-10.5-9.8-12.9
		c2.3-4.2,31.8-68.7,37.1-73.3c-2.4-2.9-23.5-36-24.4-41.5C906.5,457.1,924.4,449.3,926.5,442.5z"
                />
                <path
                  class="st7"
                  d="M926.5,442.5c3-16-21.3-62.4-42.6-52c-18.5,9.1-8.4,66-2.4,70C888.7,463.6,923.7,453.1,926.5,442.5z"
                />
                <path
                  class="st12"
                  d="M830.3,357.4c-1,3.1-1.5,12.7-0.4,17c0.1,0.2,20,1.7,22.2-1.8c0.1-2.9,4.9-28.7,11.4-36.7
		c0.6-0.9-0.7-3.4-0.7-3.4l-23.1,9.6L830.3,357.4"
                />
                <path
                  class="st2"
                  d="M860.2,334.7c1.5,2,3.4,2.9,5.1,2.9c3.8,0,12.6-3.5,12.6-16c0-9-8.8-13.6-8.8-17.9c0-4.1,1.1-4.2,1.1-7.6
		c0-1.7-1.7-7.3-7-7.3c-3,0-4.1,2.5-7.1,2.5c-3.3,0-6.3-6.4-11.3-6.4c-3.4,0-6.6,3.2-10.2,3.2c-4.1,0-6.9-6.1-12.6-6.1
		c-5.9,0-8,5.3-10.3,5.3c-2.9,0-3.4-0.8-6.3-0.8c-1.8,0-7.3,3.2-7.3,9c0,4.1,1.7,10.8,10.2,10.8c5,0,7.8,7.9,12.2,7.9
		c1.7,0,3.2-1.4,3.6-0.7c1.7,3,5.2,11.2,5.2,11.2l15.9,8.9L860.2,334.7z"
                />
                <path
                  class="st4"
                  d="M856.7,330.6c0,1.4-0.5,1.7-2.6,1.7c-1,0-2.4-1.3-2.4-2.7c0-3.3,2.4-4,2.4-8.3c0-7.3-19.1-11.1-25.8-14.9l0,0
		c-2.4,2.4-4.1,5.5-4.8,9l-4.3,22.1c-1.9,9.6,4.4,18.9,13.9,20.8s18.9-4.4,20.8-13.9l0.7-3.8l0,0c0.4,0.1,0.8,0.2,1.1,0.2
		c2.5,0,4.4-2.3,4.4-5.1C860.3,333.1,856.7,328.5,856.7,330.6z"
                />
                <path
                  class="st5"
                  d="M114.8,781.9C94.5,646,44.8,574.7,38.5,577.4c-8.9,3.9-11.5,80.2,4.4,159c0.4,0,0.7-0.1,1.1-0.1
		c4.6,0,8.3,3.7,8.3,8.3c0,1.4-0.3,2.7-0.9,3.8c2.7,1.4,4.6,4.2,4.6,7.4c0,4-2.9,7.4-6.7,8.2c4.7,18.2,10.6,36.2,17.6,52.9
		c3.6,0,44,0,44,0S117.8,801.7,114.8,781.9z"
                />
                <path
                  class="st10"
                  d="M232.3,637.8c-12.3,0-25.5,35.4-40.1,35.4c-3.2,0-5.3-3.5-5.3-6.8c0-3.2,10.1-38.4,10.1-55.5
		c0-1.5-0.1-3.1-0.3-4.7c-1.6,1-3.6,1.6-5.6,1.6c-6,0-10.9-4.9-10.9-10.9c0-5.3,3.7-9.6,8.7-10.7c-5.1-6.5-12.6-11.1-22.8-11.1
		c-12.9,0-31.1,11.5-31.1,29.3c0,5,1.5,17.7,1.5,29.2c0,65.2-51.1,75-51.1,147.2c0,15.2,8.4,31.9,10.9,36c0,0,42.8,0.5,46.9,0.5
		s37.4-55.6,41.2-61.5c14.5-22.4,62.7-47,62.7-100.5C247.1,647.8,244.4,637.8,232.3,637.8z"
                />
              </g>
            </svg>
          </div>
        </div>
      </div>
    </section>
    <!----------------------------cALL TO ACTION----------------->
    <svg
      class="wave-top"
      viewBox="0 0 1439 147"
      version="1.1"
      xmlns="http://www.w3.org/2000/svg"
      xmlns:xlink="http://www.w3.org/1999/xlink"
    >
      <g stroke="none" stroke-width="1" fill="none" fill-rule="evenodd">
        <g transform="translate(-1.000000, -14.000000)" fill-rule="nonzero">
          <g class="wave" fill="#f8fafc">
            <path
              d="M1440,84 C1383.555,64.3 1342.555,51.3 1317,45 C1259.5,30.824 1206.707,25.526 1169,22 C1129.711,18.326 1044.426,18.475 980,22 C954.25,23.409 922.25,26.742 884,32 C845.122,37.787 818.455,42.121 804,45 C776.833,50.41 728.136,61.77 713,65 C660.023,76.309 621.544,87.729 584,94 C517.525,105.104 484.525,106.438 429,108 C379.49,106.484 342.823,104.484 319,102 C278.571,97.783 231.737,88.736 205,84 C154.629,75.076 86.296,57.743 0,32 L0,0 L1440,0 L1440,84 Z"
            />
          </g>
          <g transform="translate(1.000000, 15.000000)" fill="#FFFFFF">
            <g
              transform="translate(719.500000, 68.500000) rotate(-180.000000) translate(-719.500000, -68.500000) "
            >
              <path
                d="M0,0 C90.7283404,0.927527913 147.912752,27.187927 291.910178,59.9119003 C387.908462,81.7278826 543.605069,89.334785 759,82.7326078 C469.336065,156.254352 216.336065,153.6679 0,74.9732496"
                opacity="0.100000001"
              />
              <path
                d="M100,104.708498 C277.413333,72.2345949 426.147877,52.5246657 546.203633,45.5787101 C666.259389,38.6327546 810.524845,41.7979068 979,55.0741668 C931.069965,56.122511 810.303266,74.8455141 616.699903,111.243176 C423.096539,147.640838 250.863238,145.462612 100,104.708498 Z"
                opacity="0.100000001"
              />
              <path
                d="M1046,51.6521276 C1130.83045,29.328812 1279.08318,17.607883 1439,40.1656806 L1439,120 C1271.17211,77.9435312 1140.17211,55.1609071 1046,51.6521276 Z"
                opacity="0.200000003"
              />
            </g>
          </g>
        </g>
      </g>
    </svg>
    <section class="container mx-auto text-center py-6 mb-12">
      <h1
        class="w-full my-2 text-4xl font-bold leading-tight text-center text-white px-7"
      >Become a Pilot User Now!</h1>
      <div class="w-full mb-4">
        <div class="h-1 mx-auto bg-white w-1/6 opacity-25 my-0 py-0 rounded-t"></div>
      </div>

      <p class="my-4 text-1xl leading-tight px-10 text-white">
        VoiceMe.AI is currently accepting a limited number of companies to join their pilot group.
        This is your opportunity to help tailor the platform to your companies needs.
        Lock in early adopter pricing as an added benefit. There are only four accounts left!
      </p>

      <button
        class="mx-auto lg:mx-0 hover:underline bg-white text-gray-800 font-bold rounded-full my-6 py-4 px-8 shadow-lg"
        v-scroll-to="'#requestrial'"
      >Sign up for a free pilot!</button>
    </section>
    <requestrial />
  </div>
</template>

<script>
import Navbar from "~/components/Navbar.vue";
import requestrial from "~/components/requesttrial.vue";
export default {
  components: {
    Navbar,
    requestrial
  },
  data() {
    return {
      open: false
    };
  },
  methods: {
    toggle() {
      this.open = !this.open;
    }
  }
};
</script>

<style lang="css" scoped>
.gradient {
  background: linear-gradient(90deg, #134abf 0%, #cecece 100%);
}
</style>
