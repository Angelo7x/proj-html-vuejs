<template>
  <footer>
    <div class="footer-container">
      <ul>
        <li><h3>AVADA UNIVERSITY</h3>
          <ul>
            <li v-for="(avadaElm, index) in avada" :key="index"><span v-html="avadaElm.avadaIcon"></span>  {{avadaElm.avadaLink}}</li>
          </ul>
        </li>
        <li><h3>RECENT POSTS</h3>
          <ul>
            <li v-for="(postsElm, index) in posts" :key="index">
              <a :href="postsElm.url"><span v-html="postsElm.postsIcon"></span>  {{postsElm.postsLink}}</a>
              <div>{{postsElm.date}}</div>
            </li>
          </ul>
        </li>
        <li><h3>COURSES</h3>
          <ul>
            <li v-for="(coursesElm, index) in courses" :key="index">
              <a :href="coursesElm.url">{{coursesElm.coursesLink}}</a>
            </li>
          </ul>
        </li>
        <li><h3>RESOURCES</h3>
          <ul>
            <li v-for="(resourcesElm, index) in resources" :key="index">
              <a :href="resourcesElm.url">{{resourcesElm.resourcesLink}}</a>
            </li>
          </ul>
        </li>
        <li><h3>UPCOMING EVENTS</h3>
          <ul>
            <li v-for="(eventsElm, index) in events" :key="index">
              {{eventsElm.eventsLink}}
              <div>View More...</div>
            </li>
          </ul>
        </li>
      </ul>
      <hr>
      <div class="footer-bottom">
        <div class="footer-bottom-text">
          <p>© Copyright 2012 - 2021 | Avada Theme by ThemeFusion | All Rights Reserved | Powered by WordPress</p>
        </div>
        <div class="footer-bottom-icon">
          <a href="#" title="facebook"><i class="fab fa-facebook-f"></i></a>
          <a href="#" title="twitter"><i class="fab fa-twitter"></i></a>
          <a href="#" title="youtube"><i class="fab fa-youtube"></i></a>
          <a href="#" titgle="instagram"><i class="fab fa-instagram"></i></a>
        </div>
      </div>
    </div>
  </footer>
</template>

<script>
export default {
    name: "Footer",
    data() {
      return {
        avada: [
          {
            avadaIcon: '<i class="fas fa-home"></i>',
            avadaLink: "Residential Location 9521 Broadsberry Avenue",
          },
          {
            avadaIcon: '<i class="fas fa-phone"></i>',
            avadaLink: "1.800.567.8910",
          },
          {
            avadaIcon: '<i class="fas fa-envelope"></i>',
            avadaLink: "info@your-domain.com",
          },
          {
            avadaIcon: '<i class="far fa-clock"></i>',
            avadaLink: "Monday - Friday 8:00 AM - 10:00 PM",
          },
        ],
        posts: [
          {
            postsLink: "What do successful grads think you should study?",
            url: "#",
            date: "March 16, 2016",
            postsIcon: '<i class="fas fa-angle-right"></i>',
          },
          {
            postsLink: "Former student discusses success in the fashion industry",
            url: "#",
            date: "March 16, 2016",
            postsIcon: '<i class="fas fa-angle-right"></i>',
          },
          {
            postsLink: "How do you best prepare for university?",
            url: "#",
            date: "March 16, 2016",
            postsIcon: '<i class="fas fa-angle-right"></i>',
          },
        ],
        courses: [
          {
            coursesLink: "Arts & Humanities",
            url: "#",
            
          },
          {
            coursesLink: "Business & Management",
            url: "#",
          },
          {
            coursesLink: "Engineering & Technology",
            url: "#",
          },
          {
            coursesLink: "Life Sciences & Medicine",
            url: "#",
          },
          {
            coursesLink: "Natural Sciences",
            url: "#",
          },
        ],
        resources: [
          {
            resourcesLink: "Campus Directory",
            url: "#",
          },
          {
            resourcesLink: "Academic Calendar",
            url: "#",
          },
          {
            resourcesLink: "Sport Clubs",
            url: "#",
          },
          {
            resourcesLink: "Graduate Programs",
            url: "#",
          },
          {
            resourcesLink: "Faculty & Staff",
            url: "#",
          },
        ],
        events: [
          {
            eventsLink: "Business Seminar",
          },
          {
            eventsLink: "Politics Seminar",
          },
        ]
      }
    }
}
</script>

<style lang="scss" scoped>
footer {
  background-image: url("../assets/img/university_ft_bg.png");
  background-repeat: no-repeat;
  background-position: center;
  background-size: cover;
  margin-top: 200px;
  .footer-container {
    @import '../assets/style/variables';
    hr {
      margin: 30px 0;
    }
    width: $sizeFooterContainer;
    // height: 200px;
    margin: auto;
    a {
      text-decoration: none;
      color: $firstColor;
    }
    a:hover {
      opacity: 0.6;
    }
    ul {
      display: flex;
      justify-content: space-between;
      list-style: none;
      h3 {
        color: $firstColor;
        margin-bottom: 20px;
      }
      ul {
        display: flex;
        flex-direction: column;
        div {
          color: rgb(177, 177, 177);
        }
        li {
          padding: 20px 0;
          display: inline-block;
        }
      }
    }
    .footer-bottom {
      display: flex;
      justify-content: space-between;
      padding-bottom: 40px;
      .footer-bottom-text, .footer-bottom-icon {
        color: $secondColor;
      }
      .footer-bottom-icon {
        a {
          padding: 10px;
          color: $secondColor;
        }
      }
    }
  }
}
</style>