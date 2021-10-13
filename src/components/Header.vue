<template>
  <header>
    <div class="header-top">
      <div class="header-top-left">
        <ul>
          <li v-for="(link, index) in menu" :key="index">
            <a :href="link.url"> <span v-html="link.iconLink"></span> {{link.nameLink}}</a>
          </li>
        </ul>
      </div>
      <div class="header-top-right">
        <a href="#"><i class="fab fa-facebook-f"></i></a>
        <a href="#"><i class="fab fa-twitter"></i></a>
        <a href="#"><i class="fab fa-youtube"></i></a>
        <a href="#"><i class="fab fa-instagram"></i></a>
      </div>
    </div>
    <div class="header-bottom">
      <div class="header-bottom-left">
        <img src="../assets/img/university_logo.png" alt="Logo">
      </div>
      <div class="header-bottom-right">
        <ul>
          <li v-for="(elm, index) in nav" :key="index">
            <a :href="elm.url" :class="{ active : elm.current }">{{ elm.navName }}</a>
          </li>
        </ul>
      </div>
    </div>
  </header>
</template>

<script>
export default {
    name: "Header",
    data() {
      return {
        menu: [
          {
            iconLink: '<i class="fas fa-phone"></i>',
            url: "#",
            nameLink: "1.800.567.8910",
          },
          {
            iconLink: '<i class="fas fa-envelope"></i>',
            url: "#",
            nameLink: "Contact us",
          },
          {
            iconLink: '<i class="fas fa-graduation-cap"></i>',
            url: "#",
            nameLink: "Alumni",
          },
          {
            iconLink: '<i class="fas fa-university"></i>',
            url: "#",
            nameLink: "Campus",
          },
        ],
        nav: [
          {
            navName: "HOME",
            url: "#",
            current: true,
          },
          {
            navName: "ABOUT",
            url: "#",
            current: false,
          },
          {
            navName: "COURSES",
            url: "#",
            current: false,
          },
          {
            navName: "EVENTS",
            url: "#",
            current: false,
          },
          {
            navName: "FACILITIES",
            url: "#",
            current: false,
          },
          {
            navName: "NEWS",
            url: "#",
            current: false,
          },
          {
            navName: "ADMISSIONS",
            url: "#",
            current: false,
          },
        ],
      }
    }
}
</script>

<style lang="scss" scoped>
header {
  height: 70px;
  background-color: #ffab0b;
  .header-top {
    @import '../assets/style/variables';
    width: $sizeContainer;
    height: 70px;
    margin: auto;
    color: white;
    display: flex;
    justify-content: space-between;
    align-items: center;
    .header-top-left {
      li {
        list-style: none;
        display: inline-block;
        a {
          padding: 20px;
          text-decoration: none;
          color: white;
        }
        a:hover {
          color: black;
        }
      }
    }
    .header-top-right {
      a {
        color: white;
        padding: 20px;
        text-decoration: none;
      }
      a:hover {
        color: black;
      }
    }
  }
  .header-bottom {
    @import '../assets/style/variables';
    width: $sizeContainer;
    height: 130px;
    display: flex;
    margin: auto;
    justify-content: space-between;
    align-items: center;
    .header-bottom-right {
      li {
        list-style: none;
        display: inline-block;
        a {
          padding: 20px;
          text-decoration: none;
          color: black;
        &.active {
          color: #ffab0b;
        }
        }
        a:hover {
          color: #ffab0b;
        }
      }
    }
  }
}
</style>