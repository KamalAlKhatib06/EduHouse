<template>
<div class="about-us" id="about">
    <div class="container ">
        <div class="row">
            <div class="col-lg-6 col-sm-12">
                <div class="about-banner">
                    <img src="../assets/about-banner.jpg" class="img-fluid  rounded-2 first-img" width="450" height="590">
                    <img src="../assets/about-abs-1.jpg" class="img-fluid rounded-2 second-img">
                    <img src="../assets/about-abs-2.jpg" class="img-fluid rounded-2 third-img">
                </div>
            </div>
            <div class="col-lg-6 col-sm-12">
                <div class="about-content">
                    <div class="subtitle px-auto pt-2">
                        Who We Are
                    </div>
                    <div class="title px-auto pt-1">
                        We Offer The Best Carrier
                    </div>
                    <ul class="about-list px-auto pt-1">
                        <li class="about-item" v-for="letter in letters" :key="letter.id">
                            <div class="item-icon">
                                <img :src="require(`../assets/about-icon-${letter.id}.png`)" class="img-fluid">
                            </div>
                            <div class="item-content">
                                <h3 class="item-title">
                                        {{ letter.title }}
                                </h3>
                                <p class="item-desc">
                                    {{ letter.desc }}
                                </p>
                            </div>
                        </li>
                    </ul>

                    <button class="btn main-btn about-us-btn font-weight-700 " style="margin-top:-20px; margin-left:20px;">
                    Know About Us
                    <fa icon="fa-solid fa-arrow-right-long mx-1" class="px-2"></fa>
                </button>
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
      letters: [
        {
          id: 1,
          title: 'Industry Expert Instructor',
          desc: 'Lorem ipsum dolor sit amet consectetur adipisicing elit. lorem ipsum amet consectetur adipisicing'
        },
        {
          id: 2,
          title: 'Up-to-Date Course Content',
          desc: 'Lorem ipsum dolor sit amet consectetur adipisicing elit. lorem ipsum amet consectetur adipisicing'
        },
        {
          id: 3,
          title: 'Biggest Student Community',
          desc: 'Lorem ipsum dolor sit amet consectetur adipisicing elit. lorem ipsum amet consectetur adipisicing '
        }
      ]
    }
  }
}
</script>

<style >
.about-us{
    width: 100%;
    padding-top:180px;
    height: fit-content;
    background-size:cover;
    padding-block:80px;
    padding-block-start:0;
}

.second-img{
    display:block;
    position: absolute;
    top: 50%;
    transform: translateY(-50%);
    right:-20px;
}
@media (min-width:768px) {
    .about-banner{
        margin-bottom: 25px;
        margin-inline: 20px 100px;
    }
    .third-img{
        display:block;
        position: absolute;
        top: 15%;
        left: -121px;
        z-index:-1;
    }
    .second-img {
        right: -55px;
    }
}
@media(min-width:575px) {
    .about-banner{
        position: relative;
        margin-bottom: 25px;
    }
}
@media (max-width:575px){
    .about-banner{
        margin-bottom: 25px;
    }

}
@media(max-width:760px) {
    .third-img{
        display:none
    }
}
@media(max-width:575px) {
    .second-img {
        display:none;
    }
}

.subtitle{
    font-weight:800;
    font-size: 16px;
    letter-spacing: 2px;
    text-transform: uppercase;
    line-height: 26px;
    color:#6F77E2;
    font-family: Urbanist;
    margin-left: 60px;
}
.title{
    font-weight:800;
    font-size: 40px;
    margin-block: 5px;
    line-height: 52px;
    color:#231f41;
    font-family: Urbanist;
    margin-left: 60px;
}
.about-list{
    margin-block:20px 60px;
}
.about-item{
    margin-block-end: 30px;
    display:flex;
    align-items: flex-start;
    gap: 25px;
}
.about-item .item-icon{
    padding:15px;
    background: hsl(230, 30%, 96%);
    border-radius: 50%;
    margin-top:17px;

}
.about-item .item-icon img{
    width: 40px;
}
.about-item .item-content .item-title{
    color: #231f41;
    font-size: 20px;
    font-weight:500;
    list-style: 32px;
    font-style: normal;
    line-height:1.6;
    margin-block-end:5px;
}
.about-item .item-content .item-desc{
    color:#6f6b80;
    font-weight: 400;
    line-height: 26px;
}
.about-us-btn{
    font-family:Urbanist;
    letter-spacing: 2px;
}
</style>
