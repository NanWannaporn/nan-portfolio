<template>
  <div class="section">
    <div class="container margin-tb-50">
      <div class="row d-flex flex-wrap justify-center">
        <div class="card peach-pink-bg card-radius">
          <div class="card-body ta-center d-flex wrap">
            <img :src="edu_img" class="icon-size margin-auto main-card-text" />
            <h4 class="margin-auto main-card-text">Education</h4>
            <div class="sub-card-text">
              <h4 class="light-matcha-color bold">Computer Engineering</h4>
              <h5>KKU</h5>
              <h6>2017-2020</h6>
            </div>
          </div>
        </div>
        <div class="card peach-pink-bg card-radius">
          <div class="card-body ta-center d-flex wrap">
            <img :src="exp3_img" class="icon-size margin-auto main-card-text" />
            <h4 class="margin-auto main-card-text">Experience</h4>
            <div class="sub-card-text">
              <h4 class="light-matcha-color bold">1 Year</h4>
              <h5>Developer</h5>
              <h6>Internship & Freelance</h6>
            </div>
          </div>
        </div>
        <div class="card peach-pink-bg card-radius">
          <div class="card-body ta-center d-flex wrap">
            <img
              :src="career_img"
              class="icon-size margin-auto main-card-text"
            />
            <h4 class="margin-auto main-card-text">Now</h4>

            <div class="sub-card-text">
              <h4 class="light-matcha-color bold">Programmer</h4>
              <h5>Bankok Bank</h5>
              <h6>since Jan 2022 - Now</h6>
            </div>
          </div>
        </div>
      </div>
      <div class="row ">
        <div class="col-sm-3 ">
          <img :src="img" class="img-size picture margin-auto" />
        </div>
        <div class="col-sm-9 margin-auto">
          <div class="row">
            <div class="col-sm-2">
              <p>Name</p>
              <p>Nickname</p>
              <p>Birthday</p>
              <p>Age</p>
            </div>
            <div class="col-sm-3">
              <p>Wannaporn Temsiritrakul</p>
              <p>Nan</p>
              <p>21 Dec 1998</p>
              <p>{{ myAge }}</p>
            </div>
            <div class="col-sm-2">
              <p>Name</p>
              <p>Nickname</p>
              <p>Birthday</p>
              <p>Age</p>
            </div>
            <div class="col-sm-3">
              <p>Wannaporn Temsiritrakul</p>
              <p>Nan</p>
              <p>21 Dec 1998</p>
              <p>{{ myAge }}</p>
            </div>
          </div>
          
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import nan_photo from "../assets/nan_photo.jpg";
import education from "../assets/education.png";
import career from "../assets/career.png";
import exper1 from "../assets/contact.png";
import exper2 from "../assets/signature.png";
import exper3 from "../assets/rating.png";
export default {
  name: "AboutmeSection",
  data() {
    var birthdateYear = 1998;
    var currentYear = new Date().getFullYear();
    var age = currentYear - birthdateYear;
    return {
      myAge: age,
      img: nan_photo,
      edu_img: education,
      career_img: career,
      exp1_img: exper1,
      exp2_img: exper2,
      exp3_img: exper3,
    };
  },
};
</script>

<style>
.section {
  margin: 13px;
}
.sixe-section {
  height: 200px;
}

.bold {
  font-weight: bold;
}
.picture {
  width: 200px;
  height: auto;
}
.icon-size {
  height: auto;
  width: 100px;
}
.wrap {
  flex-wrap: wrap;
}
.pad-5 {
  padding: 5px;
}
.main-card-text {
  color: #c79a96;
  font-weight: bold;
}
/* hover */
.sub-card-text {
  display: none;
  margin: auto;
}
.card:hover .sub-card-text {
  display: block;
  color: white;
}
.card:hover .main-card-text {
  display: none;
}
</style>
