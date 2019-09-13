<template>
  <div class="gradient">
    <Navbar />
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
#menu-toggle:checked + #menu {
  display: block;
}
.gradient {
  background: linear-gradient(90deg, #134abf 0%, #cecece 100%);
}
</style>
