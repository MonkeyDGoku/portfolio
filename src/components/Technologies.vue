<template>
  <div class="techno container-fluid">
    <div class="techno__header">
      <h1>Technologies</h1>
    </div>
    <div class="container-fluid">
      <div class="row techno__content">
        <div class="col-md-6 techno-detail">
          <div class="techno__items">
            <div class="techno__item container-fluid">
              <div class="row">
                <div class="techno__item__detail col-sm-3">
                  <h3 class="techno__item__detail__desc">Server-Side</h3>
                </div>
                <div class="techno__item__logos col-sm-9">
                  <IconWrapper imgsrc="backend/logo-api.png" />
                  <IconWrapper imgsrc="backend/logo-asp-dotnet.jpg" />
                  <IconWrapper imgsrc="backend/logo-csharp.png" />
                  <IconWrapper imgsrc="backend/logo-dot-netcore.png" />
                  <IconWrapper imgsrc="backend/logo-ef-core.png" />
                  <IconWrapper imgsrc="backend/logo-sharepoint.png" />
                </div>
              </div>
            </div>
            <div class="techno__item container-fluid">
              <div class="row">
                <div class="techno__item__detail col-sm-3">
                  <h3 class="techno__item__detail__desc">Client-Side</h3>
                </div>
                <div class="techno__item__logos col-sm-9">
                  <IconWrapper imgsrc="frontend/logo-html.png" />
                  <IconWrapper imgsrc="frontend/logo-javascript.png" />
                  <IconWrapper imgsrc="frontend/logo-bootstrap.png" />
                  <IconWrapper imgsrc="frontend/logo-materail-ui.png" />
                  <IconWrapper imgsrc="frontend/logo-reactjs.png" />
                  <IconWrapper imgsrc="frontend/logo-vuejs.png" />
                </div>
              </div>
            </div>
            <div class="techno__item container-fluid">
              <div class="row">
                <div class="techno__item__detail col-sm-3">
                  <h3 class="techno__item__detail__desc">Database</h3>
                </div>
                <div class="techno__item__logos col-sm-9">
                  <IconWrapper imgsrc="database/logo-mysql.png" />
                  <IconWrapper imgsrc="database/oracle-sql-logo.jpg" />
                </div>
              </div>
            </div>
            <div class="techno__item container-fluid">
              <div class="row">
                <div class="techno__item__detail col-sm-3">
                  <h3 class="techno__item__detail__desc">Tools/Frameworks</h3>
                </div>
                <div class="techno__item__logos col-sm-9">
                  <IconWrapper imgsrc="tools/logo-github.png" />
                  <IconWrapper imgsrc="tools/logo-azure-ado.png" />
                  <IconWrapper imgsrc="tools/logo-docker.png" />
                  <IconWrapper imgsrc="tools/logo-pega.png" />
                  <IconWrapper imgsrc="tools/logo-sonarqube.png" />
                  <IconWrapper imgsrc="tools/logo-whitesource.png" />
                </div>
              </div>
            </div>
          </div>
        </div>
        <div class="col-md-6 social-media">
          <div class="social-media__blend"></div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import IconWrapper from "../components/IconWrapper.vue";
export default {
  components: { IconWrapper },
  name: "Technologies",
  data() {
    return {
      backend: {
        api: "backend/logo-api.png",
        aspDotNet: "../assets/images/backend/logo-asp-dotnet.jpg",
      },
      frontend: {},
      database: {},
      tools: {},
    };
  },
};
</script>

<style>
.techno {
  background: #181f28;
  display: flex;
  flex-direction: column;
  align-items: center;
}
.techno__header {
  color: white;
}
.techno__content {
  width: 100%;
}
.social-media {
  height: 500px;
  position: relative;
  background-image: url("../assets/images/dp-edited.jpg");
  background-repeat: no-repeat;
  background-size: cover;
  border-radius: 10px;
}
.social-media__blend {
  content: "";
  position: relative;
  width: 100%;
  height: 100%;
}

.techno-detail {
  height: 1000px;
}

.techno__items {
  width: 100%;
  display: flex;
  flex-direction: column;
  align-items: center;
}
.techno__item {
  background: rgb(101, 100, 98);
  width: 100%;
  height: 150px;
  margin-bottom: 10px;
  border-radius: 10px;
}
.techno__item__detail {
  content: "";
  width: 30%;
  height: 100%;
  position: relative;
}

.techno__item__detail__desc {
  position: absolute;
  top: 10px;
  color: white;
  font-size: 1.5rem;
}
.techno__item__logos {
  position: relative;
  top: 50px;
  display: flex;
  justify-content: flex-start;
  align-items: center;
  overflow: scroll;
  overflow-x: scroll;
  overflow-y: hidden;
}
.techno__item__logos::-webkit-scrollbar {
  display: none;
}
/* .icon-wrapper {
  position: relative;
  width: 50px;
  height: 50px;
  background-image: url("../assets/images/backend/logo-api.png");
  background-color: black;
  background-position: center;
  background-size: cover;
  background-repeat: no-repeat;
  border-radius: 50%;
} */
</style>
