<template>
  <Gsap msg="GSAP Sandbox" />
</template>

<script>
import Gsap from "./components/Gsap.vue";

export default {
  name: "App",
  components: {
    Gsap,
  },
};
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
