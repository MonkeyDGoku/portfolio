<template>
  <div class="icon-wrapper">
    <img class="icon-wrapper-img" :src="require(`@/assets/images/${imgsrc}`)" />
    <div class="icon-wrapper-img-cover"></div>
  </div>
</template>

<script>
export default {
  name: "ImageWrapper",
  props: {
    imgsrc: {
      type: String,
      require: true,
    },
  },
  methods: {
    imageUrl: function (path) {
      debugger;
      let image = require.context("../assets/", false, /\.png$|\.jpg$/);
      return image("./" + path);
    },
  },
};
</script>

<style>
.icon-wrapper {
  position: relative;
}
.icon-wrapper-img {
  background-color: #c5c5c3;
  width: 70px;
  height: 70px;
  border-radius: 50%;
  margin: 5px;
  object-fit: cover;
}
.icon-wrapper-img-cover {
  position: relative;
  top: -75px;
  left: 5px;
  content: "";
  width: 70px;
  height: 70px;
  border-radius: 50%;
}

.icon-wrapper-img-cover:hover {
  background: rgba(101, 100, 98, 0.5);
}
</style>
