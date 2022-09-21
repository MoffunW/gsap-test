<template>
  <div class="wrapper">
    <img src="../assets/bg.jpg" alt="bg" id="bg" />
    <h2 class="text" id="text">MOUNTAINS</h2>
    <img src="../assets/man.png" alt="man" id="man" />
    <img src="../assets/clouds_1.png" alt="clouds_1" id="clouds_1" />
    <img src="../assets/clouds_2.png" alt="clouds_2" id="clouds_2" />
    <img
      src="../assets/mountain_left.png"
      alt="mountain_left"
      id="mountain_left"
    />
    <img
      src="../assets/mountain_right.png"
      alt="mountain_right"
      id="mountain_right"
    />
  </div>
  <div class="second">
    <h2>TITLE TITLE TITLE TITLE</h2>
    <p>
      Lorem ipsum dolor sit amet consectetur adipisicing elit. Illo optio eum ut
      exercitationem? Aspernatur magni sint error voluptatibus qui commodi
      culpa. In nesciunt possimus dolorum provident est! Accusamus, vel. Minus.
      Lorem ipsum dolor sit amet consectetur adipisicing elit. Illo optio eum ut
      exercitationem? Aspernatur magni sint error voluptatibus qui commodi
      culpa. In nesciunt possimus dolorum provident est! Accusamus, vel. Minus.
      Lorem ipsum dolor sit amet consectetur adipisicing elit. Illo optio eum ut
      exercitationem? Aspernatur magni sint error voluptatibus qui commodi
      culpa. In nesciunt possimus dolorum provident est! Accusamus, vel. Minus.
      Lorem ipsum dolor sit amet consectetur adipisicing elit. Illo optio eum ut
      exercitationem? Aspernatur magni sint error voluptatibus qui commodi
      culpa. In nesciunt possimus dolorum provident est! Accusamus, vel. Minus.
      Lorem ipsum dolor sit amet consectetur adipisicing elit. Illo optio eum ut
      exercitationem? Aspernatur magni sint error voluptatibus qui commodi
      culpa. In nesciunt possimus dolorum provident est! Accusamus, vel. Minus.
      Lorem ipsum dolor sit amet consectetur adipisicing elit. Illo optio eum ut
      exercitationem? Aspernatur magni sint error voluptatibus qui commodi
      culpa. In nesciunt possimus dolorum provident est! Accusamus, vel. Minus.
      Lorem ipsum dolor sit amet consectetur adipisicing elit. Illo optio eum ut
      exercitationem? Aspernatur magni sint error voluptatibus qui commodi
      culpa. In nesciunt possimus dolorum provident est! Accusamus, vel. Minus.
      Lorem ipsum dolor sit amet consectetur adipisicing elit. Illo optio eum ut
      exercitationem? Aspernatur magni sint error voluptatibus qui commodi
      culpa. In nesciunt possimus dolorum provident est! Accusamus, vel. Minus.
    </p>
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
    // gsap.from(".sun", {
    //   y: 400,
    //   delay: 2
    // });
    gsap.to("#bg", {
      scrollTrigger: {
        scrub: 1
      },
      scale: 1.5
    });

    gsap.to("#man", {
      scrollTrigger: {
        scrub: 1
      },
      scale: 0.5
    });

    gsap.to("#mountain_left", {
      scrollTrigger: {
        scrub: 1
      },
      x: -500
    });

    gsap.to("#mountain_right", {
      scrollTrigger: {
        scrub: 1
      },
      x: 500
    });

    gsap.to("#clouds_1", {
      scrollTrigger: {
        scrub: 1
      },
      x: 200
    });

    gsap.to("#clouds_2", {
      scrollTrigger: {
        scrub: 1
      },
      x: -200
    });

    gsap.to("#text", {
      scrollTrigger: {
        scrub: 1
      },
      y: 100
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
  display: flex;
  justify-content: center;
  align-items: center;
  position: relative;
  width: 100%;
  height: 100vh;
  overflow: hidden;
  background: rgb(200, 200, 200);
  &::before {
    content: "";
    position: absolute;
    bottom: 0;
    left: 0;
    width: 100%;
    height: 200px;
    background: linear-gradient(to top, #fff, transparent);
    z-index: 10000;
  }
}

.wrapper img {
  position: absolute;
  top: 0;
  left: 0;
  height: 100%;
  width: 100%;
  object-fit: cover;
  pointer-events: none;
}

.text {
  position: relative;
  color: #fff;
  font-size: 10vw;
}

#man {
  transform-origin: bottom;
}

.second {
  font-size: 30px;
  height: 100vh;
  padding: 30px;
}
</style>
