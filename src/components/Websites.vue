<template>
  <div class="websites-section container-fluid">
    <div class="websites-header">
      <h1>My Projects</h1>
    </div>
    <div class="websites-content container-fluid">
      <el-carousel type="card" height="500px" :autoplay="false">
        <el-carousel-item>
          <div class="item">
            <a href="https://netflix-clone-3a5fe.web.app/" target="_blank">
              <ExternalLinkIcon class="site-link"
            /></a>

            <div class="item__content">
              A Netflix clone app integrated with Youtube apis
            </div>
            <img
              class="item__image"
              src="..\assets\images\netflix-clone-screenshot.jpg"
              alt=""
            />
          </div>
        </el-carousel-item>
        <el-carousel-item>
          <div class="item">
            <a
              href="https://airbnb-clone-lilac-two.vercel.app/"
              target="_blank"
            >
              <ExternalLinkIcon class="site-link"
            /></a>
            <div class="item__content">Airbnb clone app built on React.Js</div>
            <img
              class="item__image"
              src="..\assets\images\airbnb-clone-screenshot.jpg"
              alt=""
            />
          </div>
        </el-carousel-item>
        <el-carousel-item>
          <div class="item">
            <a
              href="tify-vue-clone-p8yc7fuxp-monkeydgoku.vercel.app/#/"
              target="_blank"
            >
              <ExternalLinkIcon class="site-link"
            /></a>
            <div class="item__content">
              Spotify clone app, real-time integratio with Spotify apis
            </div>
            <img
              class="item__image"
              src="..\assets\images\spotify-clone-screenshot.jpg"
              alt=""
            />
          </div>
        </el-carousel-item>
      </el-carousel>
    </div>
  </div>
</template>
<script>
import { ExternalLinkIcon } from "@vue-hero-icons/outline";
export default {
  components: {
    ExternalLinkIcon,
  },
};
</script>
<style>
.websites-section {
  background: #181f28;
  display: flex;
  flex-direction: column;
  align-items: center;
}
.websites-header {
  position: relative;
  top: 15px;
  color: white;
}
.websites-content {
  width: 100%;
  height: 600px;
  background: #181f28;
  display: flex;
  justify-content: center;
  align-items: center;
}
.item {
  position: relative;
  height: 100%;
}

.el-carousel {
  width: 100%;
}

.el-carousel__item {
  border-radius: 8px;
}

.is-active {
  box-shadow: 0 4px 8px 0 rgba(0, 0, 0, 0.2), 0 6px 20px 0 rgba(0, 0, 0, 0.19);
}
.item__content {
  position: absolute;
  bottom: 0;
  width: 100%;
  flex-direction: column;
  justify-content: center;
  align-items: center;
  background: rgba(0, 0, 0, 0.5);
  color: #fff;
  padding: 3px;
}

.item__image {
  width: 100%;
  height: 100%;
  object-fit: cover;
  border-top: 10px solid white;
  border-bottom: 10px solid white;
}

.el-carousel__item:nth-child(2n) {
  background-color: #99a9bf;
}

.el-carousel__item:nth-child(2n + 1) {
  background-color: #d3dce6;
}

.site-link {
  position: relative;
  right: 0;
}
</style>
