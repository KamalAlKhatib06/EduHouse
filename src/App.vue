<template>
<div id="app" style="overflow-x:hidden;">

</div>
<nav class="navbar navbar-expand-lg position-fixed w-100 " :class="{ white : !view.topOfPage} ">
        <div class="container">
            <a class="navbar-brand" href="#">
              <h2>EduHouse</h2>

            </a>
            <button class="navbar-toggler " type="button" data-bs-toggle="collapse"
                data-bs-target="#navbarSupportedContent" aria-controls="navbarSupportedContent" aria-expanded="false"
                aria-label="Toggle navigation">
                <span class="toggler-icon top-bar"></span>
                <span class="toggler-icon middle-bar"></span>
                <span class="toggler-icon bottom-bar"></span>
            </button>
            <div class="collapse navbar-collapse show-links mb-3" id="navbarSupportedContent">
                <ul class="navbar-nav d-flex gap-4 m-auto mb-2 align-items-center mb-lg-0 text-uppercase ">
                    <li class="nav-item">
                        <a class="nav-link active" aria-current="page" >Home</a>
                    </li>
                    <li class="nav-item">
                        <a class="nav-link" href="#about">About</a>
                    </li>
                    <li class="nav-item">
                        <a class="nav-link" href="#courses">Courses</a>
                    </li>
                    <li class="nav-item">
                        <a class="nav-link" href="#event">Event</a>
                    </li>
                    <li class="nav-item">
                        <a class="nav-link" href="#sub">Contact</a>
                    </li>
                </ul>
                <div class="search ps-3 pe-3 d-none d-lg-block mx-2">
                    <fa icon="magnifying-glass"></fa>
                </div>
                <a href="#" class="text-decoration-none">
                    <button class="btn nav-btn  mx-auto mb-2 align-items-center mb-lg-0 text-uppercase ">
                      <fa icon="fa-solid fa-user"></fa>
                        <span class="px-1 text-decoration-none">Login / Register</span>
                    </button>
                </a>
            </div>
        </div>
    </nav>
    <div class="scrollBtn" :class="{tr: !view.topOfPage}" @click="scrollToTop">
                <fa icon="fa-arrow-up mx-1" class="icon" ></fa>
            </div>
  <HeroAppVue />
  <AboutUs class="pt-3 pb-5"/>
  <OurCourses />
  <PopularCourses />
  <CtaBanner />
  <UpcomingEvents />
  <SubscribeLetter />
  <div class="footer">
    <div class="container">
      <div class="row">
        <div class="col-lg-4 col-md-12 col-sm-12">
          <div class="footer-title mt-md-3 mt-sm-3">
            EduHouse
          </div>
          <p class="footer-text mt-4">
            It is a long established fact that a reader will be distracted
             by the readable content of a page when
            looking at its layout. The point of using Lorem Ipsum.
          </p>
          <div class="social-media mt-4">
            <div class="social-media-item">
              <img src="../src/assets/facebook-brands.svg" class="img-fluid" alt="">
            </div>
            <div class="social-media-item">
              <img src="../src/assets/instagram-brands.svg" class="img-fluid" alt="">
            </div>
            <div class="social-media-item">
              <img src="../src/assets/pinterest-brands.svg" class="img-fluid" alt="">
            </div>
            <div class="social-media-item">
              <img src="../src/assets/linkedin-brands.svg" class="img-fluid" alt="">
            </div>
          </div>
        </div>
        <div class="col-lg-2 col-md-6 col-sm-6">
          <div class="footer-title mt-md-3 mt-sm-3">
            Explore
          </div>
          <div class="footer-item mt-4">
            <fa icon="fa-solid fa-chevron-left" class="ml-2 " />
            About Us
          </div>
          <div class="footer-item mt-4">
            <fa icon="fa-solid fa-chevron-left" class="ml-2"/>
            Upcoming Events
          </div>
          <div class="footer-item mt-4">
            <fa icon="fa-solid fa-chevron-left" class="ml-2"/>
            Blog & News
          </div>
          <div class="footer-item mt-4">
            <fa icon="fa-solid fa-chevron-left" class="ml-2"/>
            FAQ Question
          </div>
          <div class="footer-item mt-4">
            <fa icon="fa-solid fa-chevron-left" class="ml-2"/>
            Testimonial
          </div>
          <div class="footer-item mt-4">
            <fa icon="fa-solid fa-chevron-left" class="ml-2"/>
            Privacy Policy
          </div>
        </div>
        <div class="col-lg-3 col-md-6 col-sm-6  ">
          <div class="footer-title mt-sm-3 mt-md-3">
            Useful Links
          </div>
          <div class="footer-item mt-4 ">
            <fa icon="fa-solid fa-chevron-left" class="ml-2 " />
            Contact Us
          </div>
          <div class="footer-item mt-4">
            <fa icon="fa-solid fa-chevron-left" class="ml-2"/>
            Pricing Plan
          </div>
          <div class="footer-item mt-4">
            <fa icon="fa-solid fa-chevron-left" class="ml-2"/>
            Instuctor Profile
          </div>
          <div class="footer-item mt-4">
            <fa icon="fa-solid fa-chevron-left" class="ml-2"/>
            FAQ
          </div>
          <div class="footer-item mt-4">
            <fa icon="fa-solid fa-chevron-left" class="ml-2"/>
            Popular Courses
          </div>
          <div class="footer-item mt-4">
            <fa icon="fa-solid fa-chevron-left" class="ml-2"/>
            Terms & Conditions
          </div>
        </div>
        <div class="col-lg-3 col-md-6 col-sm-12">
          <div class="footer-title mt-md-3 mt-sm-3">
            Contact Info
          </div>
          <div class="footer-item mt-4 ">
            <fa icon="fa-solid fa-map-marker-alt" class="ml-2 " />
            275 Quadra Street Victoria <br> Road, New York
          </div>
          <div class="footer-item mt-4 ">
            <fa icon="fa-solid fa-phone" class="ml-2 " />
            + 1 (364) 765-7839
          </div>
          <div class="footer-item mt-4 ">
            <fa icon="fa-solid fa-phone" class="ml-2 " />
            + 1 (364) 765-7840
          </div>
          <div class="footer-item mt-4 ">
            <fa icon="fa-solid fa-message" class="ml-2 " />
            contact@eduhouse212.com
          </div>
        </div>
      </div>
      <div class="footer-end content text-center " style="font-size:20px; margin-top:80px">
        Copyright 2022 EduHouse. All Rights Reserved by  <span style="font-weight:bold;">KamalAlKhatib ✨</span>
      </div>
    </div>
  </div>
  <!-- <nav>
    <router-link to="/">Home</router-link> |
    <router-link to="/about">About</router-link>
  </nav>
  <router-view></router-view> -->
</template>
<script>
import HeroAppVue from './components/HeroApp.vue'
import AboutUs from './components/AboutUs.vue'
import OurCourses from './components/OurCourses.vue'
import PopularCourses from './components/PopularCourses.vue'
import CtaBanner from './components/CtaBanner.vue'
import UpcomingEvents from './components/UpcomingEvents.vue'
import SubscribeLetter from './components/SubscribeLetter.vue'
export default {
  components: {
    HeroAppVue,
    AboutUs,
    OurCourses,
    PopularCourses,
    CtaBanner,
    UpcomingEvents,
    SubscribeLetter
  },
  data () {
    return {
      view: {
        topOfPage: true
      }
    }
  },
  beforeMount () {
    window.addEventListener('scroll', this.handleScroll)
  },
  methods: {
    handleScroll () {
      if (window.pageYOffset > 80) {
        if (this.view.topOfPage) {
          this.view.topOfPage = false
        }
      } else {
        this.view.topOfPage = true
      }
    },
    scrollToTop () {
      document.body.scrollTop = 0
      document.documentElement.scrollTop = 0
    }
  }
}

</script>

<style>
*{
  margin:0;
  padding:0;
  box-sizing: border-box;
}
@font-face {
  font-family: "Urbanist";
  src: local("Urbanist")
  url(./fonts/static/Urbanist-Bold.ttf)
  format("truetype");
}
.navbar{
  position: relative;
  transition:.2s;
  z-index:5;
}
.nav-item{
  margin-bottom: 4px;
}
nav.white{
  background-color:white;
  box-shadow: 0 0 10px #aaa;
}
.search{
  background: #fff;
  padding: 17px;
  border-radius: 6px;
  color:hsl(235, 70%, 60%);
  font-size: 12px;
  position: relative;
  cursor: pointer;
}

nav .navbar-brand h2{
  font-weight:bold;
  line-height:75px;
  font-family:Urbanist;
  padding-inline:10px;
  color: hsl(235, 70%, 60%);
}

.navbar-toggler {
    border: 0 !important;
}

.navbar-toggler:focus,
.navbar-toggler:active,
.navbar-toggler-icon:focus {
    outline: none !important;
    box-shadow: none !important;
    border: 0 !important;
}

.toggler-icon {
    width: 30px;
    height: 3px;
    background-color: #e74c3c;
    display: block;
    transition: all 0.2s;
}

.middle-bar {
    margin: 5px auto;
}

.navbar-toggler .top-bar {
    transform: rotate(45deg);
    transform-origin: 10% 10%;
}

.navbar-toggler .middle-bar {
    opacity: 0;
    filter: alpha(opacity=0);
}

.navbar-toggler .bottom-bar {
    transform: rotate(-45deg);
    transform-origin: 10% 90%;
}

.navbar-toggler.collapsed .top-bar {
    transform: rotate(0);
}

.navbar-toggler.collapsed .middle-bar {
    opacity: 1;
    filter: alpha(opacity=100);
}

.navbar-toggler.collapsed .bottom-bar {
    transform: rotate(0);
}

.navbar-toggler.collapsed .toggler-icon {
    background-color: grey;
}

.navbar-collapse {
    transition: .2s cubic-bezier(0.215, 0.610, 0.355, 1);
}

.show {
    background-color: white;
    text-align: center;
    padding: 2rem;
}

.nav-item a {
  color: hsl(247, 35%, 19%);
  font-weight: 600;
  padding-inline: 10px;
  font-size: 16px;
  font-family:Urbanist;
  cursor: pointer;
}
.nav-item a:hover {
  color: hsl(235, 70%, 60%);
}

.nav-btn{
  background: hsl(235, 70%, 60%);
  color:white;
  padding:.8rem;
  font-family:Urbanist;
  font-weight:700;
  line-height:26px;
  display: flex;
  align-items: center;
  letter-spacing: 1px;
}
.nav-btn:hover,.nav-btn:focus{
  background: hsl(247, 35%, 19%);
  color:white;
  box-shadow: none;
}

.main-btn{
  background: hsl(235, 70%, 60%);
  color:white;
display: flex;
align-items: center;
  font-weight: 600;
  padding: 12px;
  padding-inline:25px;
  min-height: 60px;
  max-width: max-content;
  gap: 10px;
  border-radius: 6px;
  transition: .25 ease;
}
.main-btn a{
  text-decoration: none;
}

.main-btn:hover, .main-btn:focus{
  background: hsl(247, 35%, 19%);
  color:white;
  box-shadow: none;
}

.scrollBtn{
  position: fixed;
  right: 20px;
  width: 40px;
  color: white;
  height: 40px;
  bottom:20px;
  border-radius: 45%;
  cursor:pointer;
  transition:.2s;
  z-index: 100;
}
.scrollBtn.tr {
  background:hsl(36, 100%, 55%);

}
.scrollBtn .icon{
  position: absolute;
  top: 50%;
  left:50%;
  transform: translate(-50%,-50%);
}

.footer{
  font-family:Urbanist, sans-serif;
  padding-block-start: 140px;
  padding-block-end:80px;
  width: 100vw;
  height: fit-content;
  background: #231F41;
  color:white;
  background-size: cover;
  overflow-x: hidden;
}
.footer-title{
  font-weight:800;
  font-size:24px;
  line-height: 38px;
}
.footer-text{
  font-size:18px;
  font-weight:500;
  line-height:26px;
  font-style:normal
}
.social-media{
  /* background:red; */
  display:flex;
  gap:40px;
}
.social-media-item{
  background: white;
  padding: 10px;
  border-radius: 6px;
  cursor:pointer;
}
.social-media-item img{
  width:30px;
  height:30px
}
.footer-item{
  font-size: 18px;
  cursor:pointer;
  transition:.2s;
}
.footer-item:hover{
  color:#525ee0
}
</style>
