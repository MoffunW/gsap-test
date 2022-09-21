<template>
  <MainContent />
</template>

<script>
// import { gsap } from "gsap";
import MainContent from "./components/MainContent.vue";

export default {
  name: "App",
  components: {
    MainContent
  }
};
</script>

<style>
* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
  font-family: "Segoe UI", Tahoma, Geneva, Verdana, sans-serif;
}

body {
  height: 100%;
}
</style>
