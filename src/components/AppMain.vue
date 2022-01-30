<template>
  <div class="app-main">
    <section>
      <img
        :src="require('@/assets/images/bg.jpg')"
        id="bg"
        :style="{ top: bgStyle + 'px' }"
        alt="bg"
      />
      <img
        :src="require('@/assets/images/moon.png')"
        id="moon"
        :style="{ left: moonStyle + 'px' }"
        alt="moon"
      />
      <img
        :src="require('@/assets/images/mountain.png')"
        id="mountain"
        :style="{ top: mountainStyle + 'px' }"
        alt="mountain"
      />
      <img
        :src="require('@/assets/images/road.png')"
        id="road"
        :style="{ top: roadStyle + 'px' }"
        alt="road"
      />

      <h2 class="text" :style="{ top: textStyle + 'px' }">Anup Mahato</h2>
    </section>
  </div>
</template>

<script>
import Websites from "./Websites.vue";
export default {
  name: "AppMain",
  data() {
    return {
      bgStyle: 0,
      moonStyle: 0,
      mountainStyle: 0,
      roadStyle: 0,
      textStyle: 0,
    };
  },
  components: {},
  computed: {},
  created() {
    window.addEventListener("scroll", this.handleScroll);
  },
  destroyed() {
    window.removeEventListener("scroll", this.handleScroll);
  },
  methods: {
    handleScroll(event) {
      var value = window.scrollY;
      this.bgStyle = value * 0.5;
      this.moonStyle = -value * 0.5;
      this.mountainStyle = -value * 0.15;
      this.roadStyle = value * 0.15;
      this.textStyle = value;
    },
  },
};
</script>

<style>
section {
  position: relative;
  width: 100%;
  height: 100vh;
  overflow: hidden;
  display: flex;
  justify-content: center;
  align-items: center;
}

section:before {
  content: "";
  position: absolute;
  bottom: 0;
  width: 100%;
  height: 100px;
  background: linear-gradient(to top, #0a2a43, transparent);
  z-index: 10000;
}

section:after {
  content: "";
  position: absolute;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
  background: #0a2a43;
  z-index: 100;
  mix-blend-mode: color;
}

section img {
  position: absolute;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
  object-fit: cover;
  pointer-events: none;
}

.text {
  position: relative;
  color: #fff;
  font-size: 10em;
  z-index: 1;
}
.text-desc-detail {
  font-size: 5em;
}

#road {
  z-index: 2;
}
</style>
