<template>
  <section>
    <div class="first-section-hero">
      <div class="hero-text">
        <h2>Inspiring Tomorrows Leaders</h2>
        <h4>The Future Belongs To those Who See Possibilities Today</h4>
        <button class="btn orange-btn">FIND A COURSE</button>
        <button class="btn blue-btn">APPLY NOW</button>
      </div>
    </div>
  </section>
</template>

<script>
export default {
    name: "Main",
}
</script>

<style lang="scss" scoped>
section {
  margin-top: 130px;
}
.first-section-hero {
  height: 550px;
  background-image: url('../assets/img/home_main_slider_bg.jpg');
  background-repeat: no-repeat;
  background-position: center;
  object-fit: cover;
  position: relative;
  .hero-text {
    font-size: 40px;
    color: #fff;
    text-align: center;
    margin-top: auto;
  }
}
</style>