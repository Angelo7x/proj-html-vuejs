<template>
  <section>
    <!-- hero -->
    <div class="first-section-hero">
      <div class="hero-text">
        <h2>Inspiring Tomorrows Leaders</h2>
        <h4>The Future Belongs To those Who See Possibilities Today</h4>
        <button class="btn orange-btn">FIND A COURSE</button>
        <button class="btn blue-btn">APPLY NOW</button>
      </div>
    </div>
    <!-- hero -->
    <!-- Seconda sezione -->
    <div class="second-section">
      <div class="logo-section">
        <a href="#"><img src="../assets/img/page-logo-1.png" alt="logosection"></a>
        <h2>Inspired By Excellence & Innovation</h2>
        <p>We offer a wide range of hight quality of teaching and extra-curricular activities.</p>
      </div>
      <div class="middle-second-section">
        <div class="left-text">
          <h2>WHY CHOSE AVADA UNIVERSITY?</h2>
          <p>We offer a range of training packages in a range of subject areas and can offer blended learning opportunities to best meet your needs. If sitting in a room with a trainer and having the opportunity for discussion with other learners sounds good to you then we can offer this. If you prefer to study in your own time and at your own speed then one of our world class facilities.</p>
          <p>If you prefer to study in your own time and at your own speed then one of our e-learning packages may be right up your street. There is a third option, which is you like the sound of both but perhaps can’t attend all training sessions, this is when blended learning comes into its own</p>
        </div>
        <div class="right-video">
          <img width="500" height="300" src="../assets/img/business_seminar_event_feat-600x402.jpg" alt="img">
        </div>
      </div>
    </div>
    <div class="third-section">
      <div class="third-container">
        <div class="third-left">
          <h2>WORLD CLASS FACILITIES</h2>
          <p>Avada University is devoted to excellence in teaching, learning, and research, and developing leaders in many disciplines who make a difference globally.</p>
          <div>
            <div><i class="fas fa-globe"></i> <h3>International focus</h3> <span>– our students come from across the globe</span> </div>
            <div><i class="fas fa-graduation-cap"></i> <h3>International focus</h3> <span>– our students come from across the globe</span> </div>
            <div><i class="far fa-address-card"></i> <h3>International focus</h3> <span>– our students come from across the globe</span> </div>
          </div>
          <p>If you prefer to study in your own time and at your own speed then one of our e-learning packages may be right up your street.</p>
        </div>
        <div class="third-right">
          <h2>OUR VALUES</h2>
          <ul>
            <li v-for="(text, index) in ourValues" :key="index">
              <a :href="text.url"> <span v-html="text.valuesIcon"></span> {{text.valuesText}}</a>
            </li>
          </ul>
        </div>
      </div>
    </div>
  </section>
</template>

<script>
export default {
    name: "Main",
    data() {
      return {
        ourValues: [
          {
            valuesIcon: '<i class="fas fa-plus"></i>',
            url: "#",
            valuesText: "OUR MISSION",
          },
          {
            valuesIcon: '<i class="fas fa-plus"></i>',
            url: "#",
            valuesText: "OUR PHILOSOPHY",
          },
          {
            valuesIcon: '<i class="fas fa-plus"></i>',
            url: "#",
            valuesText: "OUR COMMITMENT",
          },
          {
            valuesIcon: '<i class="fas fa-plus"></i>',
            url: "#",
            valuesText: "OUR PROMISE",
          },
          {
            valuesIcon: '<i class="fas fa-plus"></i>',
            url: "#",
            valuesText: "OUR VALUES",
          },
        ]
      }
    }
}
</script>

<style lang="scss" scoped>
@import '../assets/style/variables';
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
    position: absolute;
    font-size: 40px;
    color: #fff;
    top: 50%;
    left: 50%;
    transform: translate(-50%, -50%);
    text-align: center;
    .btn {
      margin-right: 20px;
    }
    .btn:hover {
      background-color: black;
      cursor: pointer;
    }
  }
}
.second-section {
  margin-top: 50px;
  .logo-section {
    margin-bottom: 70px;
    text-align: center;
    color: $firstColor;
    h2 {
      margin: 15px 0;
    }
    p {
      color: #7e8890;
    }
  }
  .middle-second-section {
    width: $sizeContainer;
    display: flex;
    margin: auto;
    height: 500px;
    img {
      margin-left: 30px;
    }
    h2 {
      color: $firstColor;
    }
    p {
      color: $secondColor;
      margin-top: 20px;
      line-height: 34px;
    }
  }
}

.third-section {
  background-color: #f7f5f4;
  height: 600px;
  .third-container {
    width: $sizeContainer;
    display: flex;
    margin: auto;
    padding: 100px 0;
    .third-left {
      width: 50%;
      div {
        margin: 30px 0;
      }
      h3 {
        display: inline-block;
        color: $firstColor;
        margin: 0 10px;
        padding: 13px;
      }
      i {
        color: $thirdColor;
      }
      span, p {
        color: $secondColor;
      }
      p {
        margin-top: 30px;
      }
    }
    .third-right {
      width: 50%;
      margin-left: 30px;
      h2 {
        color: $firstColor;
      }
      li {
        list-style: none;
        padding: 27px 0;
        background-color: #fff;
        margin-bottom: 5px;
        padding-left: 30px;
      }
      a {
        text-decoration: none;
        color: $thirdColor;
        padding: 30px 0;
        span {
          margin-right: 20px;
        }
      }
    }
  }
}
</style>