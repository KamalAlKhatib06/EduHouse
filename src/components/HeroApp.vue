<template>
  <div class="hero-app mb-5" id="home">
    <div class="hero d-flex align-items-center mb-5" id="hero">
        <div class="container mb-5">
            <div class="row mt-5">
              <div class="col-lg-6 col-sm-12">
                <div class="hero-content">
                    <h5 class="hero-subtitle mt-5">BETTER LEARNING FUTURE WITH US</h5>
                    <div class=" display-3 fw-bold hero-title lh-1">Education Is <br> About Academic Excellence</div>
                </div>
                    <p class="hero-text">Sed eu volutpat arcu, a tincidunt nulla quam, feugiat sit amet ipsum a, dapibus porta velit.</p>
                <button class="btn main-btn d-flex align-items-center font-weight-700 ">
                  Get Started Today
                    <fa icon="fa-solid fa-arrow-right-long mx-1" class="px-2"></fa>
                </button>
              </div>
              <div class="col-lg-6 col-sm-12">
                  <img src="../assets/hero-banner.png" alt="" class="mt-4 img-fluid hero-img">
              </div>
            </div>

        </div>
    </div>
  </div>
</template>

<script>

export default {
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
      if (window.pageYOffset < 550) {
        this.view.topOfPage = false
      } else {
        this.view.topOfPage = true
      }
    }

  }

}

</script>

<style>
.hero-app{
  font-family:Urbanist, sans-serif;
  padding-block-start: 140px;
  padding-block-end:80px;
  width: 100vw;
  height: fit-content;
  background-image:url(../assets/hero-bg.jpg);
  background-size: cover;
  overflow-x: hidden;
}
.hero-title{
  font-size: 68px;
  font-weight: 800;
  color: #231f41;
  line-height: 88px;
  margin: 25px 0;
}

.hero-subtitle{
  font-size: 16px;
  font-weight: 800;
  color: hsl(235, 70%, 60%);
  line-height: 26px;
  letter-spacing: 4px;
}
.hero-text{
  color: #6f6b80;
  font-size: 20px;
  font-weight: 500;
  line-height: 38px;
}

@media (max-width:400px) {
  .hero-img{
    width: 300px;
    height:300px;
    margin-top: 20px;
  }
  .hero-title{
    font-size: 42px;
  }
  .hero-text{
    font-size: 16px;
  }
}
@media(max-width:450px){
  .hero-title{
    font-size: 54px;
  }
  .hero-text{
    font-size: 18px;
  }
}
</style>
