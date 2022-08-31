<template>
    <div class="cta" style="background-image:url('https://codewithsadee.github.io/eduhome/assets/images/cta-bg.png')">

    <div class="container">
        <div class="row">
            <div class="col-lg-6 col-sm-12">
                <div class="subtitle">
                    Free WorkShop
                </div>
                <div class="title">
                    Join Our Free Workshops
                </div>
                <p class="mt-4">
                    Lorem ipsum dolor sit amet, consectetur adipiscing elit. Sit amet,
                    consect adipi scing elit, sed do eiusmod tempor incididunt ut sed do
                    eiusmod tempor incididunt ut labore et dolore aliqua.
                </p>
                <button class="btn main-btn mt-4" style="font-family:Urbanist; letter-spacing:1px;">
                    Upcoming Workshops
                    <fa icon="fa-solid fa-arrow-right-long mx-1" class="px-2"></fa>
                </button>
            </div>
            <div class="col-lg-6 col-md-12">
                <img src="../assets/cta-banner.jpg" class="img-fluid rounded-2" alt="">
            </div>
        </div>
    </div>
    </div>
</template>

<script>
export default {

}
</script>

<style scoped>
.cta{
    width: 100%;
  padding-top: 180px;
  height: fit-content;
  background-size:cover;
  padding-block: 80px;
  background: hsl(235, 70%, 60%) top no-repeat;
  padding-block-start:100px;
}
.subtitle,.title{
    color:white;
    margin-left:25px;
    font-weight:bold;
}
p{
    font-weight:500;
    margin-block: 5px;
    line-height: 26px;
    color:White;
    font-family: Urbanist;
    margin-left:25px;
}
.main-btn{
    background:white;
    margin-left:25px;
    margin-bottom: 20px;
    color: hsl(235, 70%, 60%);
    font-weight: 700;
    font-family:Urbanist;
}
.main-btn:hover{
    background:#F76D02;
}
</style>
