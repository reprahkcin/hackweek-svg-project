<template>
  <div>
    <transition appear @before-enter="beforeEnter" @enter="enter">
      <h3>{{ msg }}</h3>
    </transition>
  </div>
</template>

<script>
import gsap from "gsap";

export default {
  name: "GSAP Sandbox",
  props: {
    msg: String,
  },

  setup() {
    const beforeEnter = (el) => {
      gsap.set(el, {
        opacity: 0,
        y: -100,
      });
    };
    const enter = (el, done) => {
      gsap.to(el, {
        duration: 1,
        opacity: 1,
        y: 0,
        onComplete: done,
        ease: "bounce.out",
      });
    };

    return {
      beforeEnter,
      enter,
    };
  },
};
</script>

<style>
</style>