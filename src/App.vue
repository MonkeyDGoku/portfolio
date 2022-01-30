<template>
  <div id="app">
    <Header />
    <app-main />
    <Websites />
    <Technologies />
  </div>
</template>

<script>
import AppMain from "./components/AppMain.vue";
import Header from "./components/Header.vue";
import Websites from "./components/Websites.vue";
import Technologies from "./components/Technologies.vue";
export default {
  name: "App",
  components: {
    AppMain,
    Header,
    Websites,
    Technologies,
  },
};
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
}

.websites-header {
  background: #181f28;
  color: white;
}
</style>
