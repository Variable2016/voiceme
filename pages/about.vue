<template>
  <div class="gradient">
    <Navbar />
    <header class="container mx-auto">
      <h3 class>About VoiceMe</h3>
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
