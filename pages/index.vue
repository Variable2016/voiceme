<template>
  <div class="gradient">
    <Navbar />
    <HeaderHome />
    <HowItWorks />
    <OurSolution />
    <CallToAction />
    <requesttrial />
    <Footer />
  </div>
</template>

<script>
import Navbar from "~/components/Navbar.vue";
import HeaderHome from "~/components/HeaderHome.vue";
import OurSolution from "~/components/OurSolution.vue";
import HowItWorks from "~/components/HowItWorks.vue";
import CallToAction from "~/components/CallToAction.vue";
import Footer from "~/components/Footer.vue";
import requesttrial from "~/components/requesttrial.vue";
export default {
  components: {
    Navbar,
    HeaderHome,
    OurSolution,
    HowItWorks,
    CallToAction,
    Footer,
    requesttrial
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
  },
  mounted: function() {}
};
</script>

<style lang="css" scoped>
.gradient {
  background: linear-gradient(90deg, #134abf 0%, #cecece 100%);
  font-family: "Manjari", sans-serif;
}
.video-house {
  position: relative;
}
.video-section {
  position: absolute;
  top: 50%;
  left: 50%;
  transform: translate(-50%, -50%);
}
</style>
