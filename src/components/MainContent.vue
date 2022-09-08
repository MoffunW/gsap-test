<template>
  <div class="wrapper">
    <div class="content">
      <div data-speed="0.5" class="sky">
        <!-- <div class="birds">
        <div class="bird">b</div>
        <div class="bird">b</div>
        <div class="bird">b</div>
      </div> -->
      </div>
      <div data-speed="0.8" class="sun">
        <img src="../assets/sun.png" alt="" />
      </div>
      <div data-speed="0.1" class="mountain">
        <img src="../assets/mountains.png" alt="" />
      </div>
      <div class="section"></div>
    </div>
  </div>
</template>

<script>
import { gsap } from "gsap";
import { ScrollTrigger } from "gsap/ScrollTrigger";

gsap.registerPlugin(ScrollTrigger);

// let smoother = ScrollSmoother.create({
//   wrapper: "wrapper",
//   content: "content",
//   smooth: 2
// });

// smoother.effects(".sun", {
//   speed: 0.5
// });

export default {
  name: "MainContent",
  props: {
    msg: String
  },
  mounted() {
    gsap.from(".sun", {
      y: 400,
      delay: 2
    });
    gsap.to(".sun", {
      y: 100,
      delay: 2,
      duration: 4,
      repeat: -1,
      yoyoEase: true
    });
    // scrollTrigger.create({trigger:'.mountain', })
  }
};
</script>

<style lang="scss" scoped>
.content {
  height: 100%;
  width: 100%;
}

.wrapper {
  padding-top: 100px;
  // height: 300vh;
  height: 100vh;
  width: 100%;
  min-height: 768px;
  background: rgb(255, 174, 107);
  overflow-x: hidden;
}

.sun {
  // position: absolute;
  // left: 50%;
  // top: 250px;
  // transform: translate(-50%);
  display: flex;
  justify-content: center;
  align-items: center;
}

.sun img {
  // position: absolute;
  height: 150px;
}

.mountain {
  align-self: end;
}

.mountain img {
  scale: 1.02;
  width: 100%;
}

.section {
  height: 100vh;
  background: #2a1e1e;
}
</style>
