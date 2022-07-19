<template>
  <div>
    <nav class="navbar navbar-expand-sm peach-pink-bg fixed-top">
      <div class="container">
        <a class="navbar-brand logo-text kindly-font hover-is-matcha" href="#">WanT</a>
        <button
          class="navbar-toggler"
          type="button"
          data-bs-toggle="collapse"
          data-bs-target="#navbarNav"
          aria-controls="navbarNav"
          aria-expanded="false"
          aria-label="Toggle navigation"
        >
          <span class="navbar-toggler-icon"></span>
        </button>

        <div class="collapse navbar-collapse display-content" id="navbarNav">
          <ul class="navbar-nav">
            <li class="nav-item active margin-auto">
              <a class="nav-link margin-auto text-bold" href="#">Home </a>
            </li>
            <li class="nav-item margin-auto">
              <a class="nav-link text-bold" href="#">About me</a>
            </li>
            <li class="nav-item margin-auto">
              <a class="nav-link text-bold" href="#">Skills</a>
            </li>
            <li class="nav-item margin-auto">
              <a class="nav-link text-bold" href="#">Work&Experience</a>
            </li>
            <li class="nav-item margin-auto">
              <a class="nav-link text-bold" href="#">Contact</a>
            </li>
          </ul>
        </div>
      </div>
    </nav>
  </div>
</template>

<script>
export default {
  name: "NavBar",
  data() {
    return {
      message: "Hi! There",
    };
  },
};
</script>

<style>

.nav-link:hover, .logo-text {
  color: #C79A96;
  font-weight: 800;
}
.text-bold{
    font-weight: bold;
}
.display-content{
    justify-content: flex-end;
}
/* .bg-color{
    --bs-bg-opacity: 1;
    background-color: #FCEDE8;
} */

</style>
