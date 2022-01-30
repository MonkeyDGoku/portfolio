<template>
  <div class="icon-wrapper">
    <img class="icon-wrapper-img" :src="require(`@/assets/images/${imgsrc}`)" />
    <div class="icon-wrapper-img-cover">
      <h6 class="icon-wrapper-img-txt"></h6>
    </div>
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
    imgtxt: {
      type: String,
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
  background: rgba(0, 0, 0, 0.2);
  box-shadow: 0 0 5px 2px white;
}

.icon-wrapper-img-txt {
  position: absolute;
  color: white;
  top: 75px;
  left: 20px;
}
</style>
