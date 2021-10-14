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
        <a href="#"><img src="../assets/img/page-logo-1.png" alt="logo"></a>
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
    <div class="fourth-section">
      <div class="fourth-section-hero-left">
        <div class="left-text-hero">
          <h2>COURSES</h2>
          <hr>
          <p>View More...</p>
        </div>
      </div>
      <div class="fourth-section-hero-middle">
        <div class="middle-text-hero">
          <h2>EVENTS</h2>
          <hr>
          <p>View More...</p>
        </div>
      </div>
      <div class="fourth-section-hero-right">
        <div class="right-text-hero">
          <h2>LATEST NEWS</h2>
          <hr>
          <p>View More...</p>
        </div>
      </div>
    </div>
    <div class="fifth-section">
      <div class="fifth-section-container">
        <div class="logo-section">
          <a href="#"><img src="../assets/img/page-logo-1.png" alt="logosection"></a>
          <h2>Today's University News</h2>
          <p>Covering topics from classes to politics and student organization events.</p>
          <hr>
        </div>
        <div class="img-container">
          <div class="left-img">
            <a href="#"><img src="../assets/img/news_single_post_header_1-400x222.jpg" alt="post1"></a>
            <div class="left-text">
              <h3>What do successful grads think you should study?</h3>
              <p>By admin|March 16th, 2016</p>
              <a href="#">Read More ></a>
            </div>
          </div>
          <div class="middle-img">
            <a href="#"><img src="../assets/img/news_single_post_header_2-400x222.jpg" alt="post2"></a>
            <div class="middle-text">
              <h3>Former student discusses success in the fashion industry</h3>
              <p>By admin|March 15th, 2016</p>
              <a href="#">Read More ></a>
            </div>
          </div>
          <div class="right-img">
            <a href="#"><img src="../assets/img/news_single_post_header_3-400x222.jpg" alt="post3"></a>
            <div class="right-text">
              <h3>How do you best prepare for university?</h3>
              <p>By admin|March 15th, 2016</p>
              <a href="#">Read More ></a>
            </div>
          </div>
        </div>
      </div>
    </div>
    <div class="sixth-section">
      <div class="sixth-section-container">
        <h2>Joing Over <span>500,00 Students</span> Enjoying Avada Education Now</h2>
        <p>Become Part of Avada University to Further Your Career.</p>
        <div class="input-container">
          <input type="text" name="name" placeholder="Name">
          <input type="email" name="email" placeholder="Email">
          <input type="text" name="telephone" placeholder="Telephone">
          <button class="btn orange-btn">APPLY NOW</button>
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
.fourth-section {
  height: 700px;
  width: 100%;
  display: flex;
  .fourth-section-hero-left {
    background-image: url("../assets/img/home_courses_section_bg.jpg");
    width: calc((100%) / 3);
    background-position: center;
    object-fit: cover;
    background-size: cover;
    background-repeat: no-repeat;
    position: relative;
    .left-text-hero {
      position: absolute;
      color: #fff;
      top: 50%;
      left: 50%;
      transform: translate(-50%, -50%);
      text-align: center;
      hr {
        background-color: $thirdColor;
        margin: 20px 0;
      }
    }
  }
  .fourth-section-hero-left:hover, .fourth-section-hero-middle:hover, .fourth-section-hero-right:hover  {
    transform: scale(0.8);
    transition: transform 1.3s;
    cursor: pointer;
  }
  .fourth-section-hero-middle {
    background-image: url("../assets/img/home_events_section_bg.jpg");
    width: calc((100%) / 3);
    background-position: center;
    object-fit: cover;
    background-size: cover;
    background-repeat: no-repeat;
    position: relative;
    .middle-text-hero {
      position: absolute;
      color: #fff;
      top: 50%;
      left: 50%;
      transform: translate(-50%, -50%);
      text-align: center;
      hr {
        background-color: $thirdColor;
        margin: 20px 0;
      }
    }
  }
  .fourth-section-hero-right {
    background-image: url("../assets/img/home_latest_news_section_bg.jpg");
    width: calc((100%) / 3);
    background-position: center;
    object-fit: cover;
    background-size: cover;
    background-repeat: no-repeat;
    position: relative;
    .right-text-hero {
      position: absolute;
      color: #fff;
      top: 50%;
      left: 50%;
      transform: translate(-50%, -50%);
      text-align: center;
      hr {
        background-color: $thirdColor;
        margin: 20px;
      }
    }
  }
}
.fifth-section {
  margin-top: 50px;
  height: 750px;
  background-color: #f7f5f4;
  .fifth-section-container {
    width: $sizeContainer;
    margin: auto;
    text-align: center;
    .logo-section {
    margin-bottom: 70px;
    color: $firstColor;
      h2 {
        margin: 15px 0;
      }
      p {
        color: #7e8890;
      }
      hr {
        background-color: $thirdColor;
        width: 50px;
        margin: 30px auto;
      }
    }
  }
}
.img-container {
  display: flex;
  .left-img, .middle-img, .right-img {
    background-color: #fff;
    margin-right: 30px;
  }
  .left-text, .middle-text, .right-text {
    padding: 30px;
    // background-color: #fff;
    h3 {
      color: $thirdColor;
    }
    a {
      text-decoration: none;
      color: $thirdColor;
    }
    p {
      color: $secondColor;
      margin: 10px 0;
    }
  }
}

.sixth-section {
  background-color: $firstColor;
  height: 300px;
  .sixth-section-container {
    margin: auto;
    width: $sizeContainer;
    text-align: center;
    color: #fff;
    padding: 30px;
    span {
      color: $thirdColor;
    }
    p {
      color: $secondColor;
      padding-bottom: 50px;
    }
    .input-container {
      input {
        padding: 7px 24px;
        margin-right: 10px;
        border: none;
        background-color: #444d63;
      }
      ::placeholder {
        color: #fff;
      }
    button:hover {
      background-color: #444d63;
    }
    }
  }
}
</style>