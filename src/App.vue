<template>
  <div>
    <NavBar />
    <div class="space-100"></div>
    <BannerPage />
    <AboutmeSection />
    <SkillsSection />
  </div>
</template>

<script>
// add boostrap
import "bootstrap/dist/css/bootstrap.min.css";
import "jquery/src/jquery.js";
import "bootstrap/dist/js/bootstrap.min.js";
import NavBar from "./components/NavBar.vue";
import BannerPage from "./components/BannerPage.vue";
import AboutmeSection from "./components/AboutmeSection.vue";
import SkillsSection from "./components/SkillsSection.vue";

export default {
  name: "App",
  components: {
    NavBar,
    BannerPage,
    AboutmeSection,
    SkillsSection,
  },
};
</script>

<style>
#app {
  /* font-family: Avenir, Helvetica, Arial, sans-serif; */
  font-family: "Tinos", serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  /* text-align: center; */
  /* color: #2c3e50; */
}
.kindly-font {
  font-family: "Pacifico", cursive;
}
.space-100 {
  height: 100px;
}
.margin-tb-50 {
  margin-top: 50px;
  margin-bottom: 50px;
}

/* theme color */
/* text */
.matcha-color {
  color: #999b84;
}
.rose-color {
  color: #c79a96;
}
.peach-pink-color {
  color: #fcede8;
}
.light-matcha-color {
  /* color: #d5d9a3; */
  color: #f1f5c5;
}
/* background */
.peach-pink-bg {
  background-color: #fcede8;
}
.matcha-bg {
  background-color: #999b84;
}
.rose-bg{
  background-color: #c79a96;
}
/* button */
.matcha-button {
  background-color: #999b84;
  color: white;
}
.matcha-button:hover {
  /* border-color: #999b84; */
  color: #999b84;
  font-weight: 600;
  border: 2px solid #999b84;
}

/* .display{
    display: flex;
} */
.justify-center {
  justify-content: center;
}
.margin-auto {
  margin: auto;
}
.middle-hori {
  margin-top: auto;
  margin-bottom: auto;
}
.ta-center {
  text-align: center;
}
.hover-is-matcha:hover {
  color: #999b84;
}
/* card css */
.card-radius, .card-rad-basic {
  border-radius: 15px;
  position: relative;
}
.card-radius:hover {
  transition: all 0.2s ease-out;
  box-shadow: 0px 4px 8px rgba(38, 38, 38, 0.2);
  top: -4px;
  border: 1px solid transparent;
  background-color: #c79a96;
  color: white;
}
.card {
  border-color: transparent;
  width: 200px;
  height: 200px;
  margin-top: 10px;
  margin-bottom: 10px;
  margin-left: 50px;
  margin-right: 50px;
}
</style>
