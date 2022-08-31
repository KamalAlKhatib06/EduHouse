<template>

  <div class="popular-courses" id="courses">

<div class="container">
    <div class="content text-center">
        <div class="subtitle">Popular Courses</div>
        <div class="title">Our Popular Courses</div>
    </div>
    <div class="row">

      <div class="col-lg-4 col-md-6 col-sm-12" v-for="cardCont in cardsCont" :key="cardCont.id">
        <div class="card mt-5"  :data-level="cardCont.level">
        <figure class="card-banner">
          <img class="card-img img-rel img-fluid" :src="require(`../assets/course-${cardCont.id}.jpg`)">
        </figure>
          <div class="card-icon" @click="changeIconColor">
            <fa icon="fa-solid fa-heart" />
          </div>
  <div class="card-body card-top d-flex gap-5">
    <div class="lessons">
      <fa icon="fa-book" />
      {{ cardCont.lessons }} Lessons
      </div>
    <div class="time">
      <fa icon="fa-clock" />
       {{ cardCont.time }}
      </div>
    </div>
    <div class="card-body ">
      <div class="card-title">
        {{ cardCont.title }}
      </div>
      <div class="reviews pt-3 text-black-50">
        <fa icon="fa-star" v-for="star in 5" :key="star" class="text-warning"/>
        ({{cardCont.reviews}} reviews)
      </div>
    </div>
  <div class="card-footer">
    <div class="salary ">
      <span class="new">{{ cardCont.newPrice }}</span>
      <span class="old">{{ cardCont.oldPrice }}</span>
    </div>
    <div class="students">
      <fa icon="fa-user" />
      <span>
        {{ cardCont.students }}
      </span>
    </div>
  </div>
</div>
      </div>
      </div>
      <div class="content text-center">
        <button class="btn main-btn font-weight-700  mt-4 " style="font-family:Urbanist; letter-spacing:2px;">
          View All Courses
          <fa icon="fa-solid fa-arrow-right-long mx-1" class="px-2"></fa>
        </button>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  data () {
    return {
      cardsCont: [
        {
          id: 1,
          level: 'Advanced',
          img: '../assets/course-2.jpg',
          lessons: 35,
          time: '18h 15m 44s',
          title: 'Competitive Strategy law for all students',
          reviews: 18,
          oldPrice: '$39.99',
          newPrice: '$29.99',
          students: '244 Students'
        },
        {
          id: 2,
          level: 'Intermediate',
          lessons: 32,
          time: '12h 15m 44s',
          title: 'Machine Learning A-Z: Hands-On Python and java',
          reviews: 12,
          oldPrice: '$19.99',
          newPrice: '$9.99',
          students: '64 Students'
        },
        {
          id: 3,
          level: 'Advanced',
          lessons: 65,
          time: '28h 25m 44s',
          title: 'Dropshipping , AmazonFBA (From Zero to Hero)  ',
          reviews: 668,
          oldPrice: '$59.99',
          newPrice: '$49.99',
          students: '1189 Students'
        },
        {
          id: 4,
          level: 'Basic',
          lessons: 18,
          time: '5h 45m 52s',
          title: 'Achieving Advanced in Insights With Big Developments',
          reviews: 13,
          oldPrice: '$19.99',
          newPrice: '$9.99',
          students: '136 Students'
        },
        {
          id: 5,
          level: 'Basic',
          lessons: 18,
          time: '5h 45m 52s',
          title: 'Marketing Research: support your marketing decisions',
          reviews: 132,
          oldPrice: '$59.99',
          newPrice: '$39.99',
          students: '166 Students'
        },
        {
          id: 6,
          level: 'Intermediate',
          lessons: 58,
          time: '19h 45m 52s',
          title: 'Write Article Content for SEO and Affiliate Marketing Course',
          reviews: 363,
          oldPrice: '$29.99',
          newPrice: '$19.99',
          students: '436 Students'
        }
      ]
    }
  },
  methods: {
    changeIconColor (e) {
      e.currentTarget.classList.toggle('red')
    }
  }
}
</script>

<style scoped>
.main-btn{
  margin-inline:auto;
  margin-top: 40px;
}
.popular-courses{
    width: 100%;
  padding-top: 180px;
  height: fit-content;
  background-size:cover;
  padding-block: 80px;
  padding-block-start:100px;
}
.img-rel{
    position: relative;
}
.card::before{
    content:attr(data-level);
    position:absolute;
    width: 100px;
    font-family:Urbanist;
    height: 25px;
    border-radius:s6px;
    background: white;
    top: 20px;
    padding: 6px;
    font-weight: 500;
    font-size: 14px;
    line-height: 22px;
    letter-spacing: 1px;
    left: 20px;
    color:#525ee0;
    z-index:4;
    display:flex;
    justify-content: center;
    align-items: center;
}.card .card-icon.red {
  color: red;
}
.card{
  overflow: hidden;
}
.card .card-icon {
    position: absolute;
    height: 30px;
    display:flex;
    justify-content: center;
    align-items: center;
    width: 30px;
    color: white;
    border-radius:50%;
    background: #525ee02a;
    right: 20px;
    cursor: pointer;
    top: 20px;
}
.card-banner{
  aspect-ratio: 370 / 270;
  overflow:hidden;

}
.card-banner img{
  transition:0.5s ease ;
}
.card:is(:hover, :focus-within) .img-rel{
  transition: 0.5s ease;
  transform: scale(1.1);
  overflow:hidden;
  cursor: pointer;
}

.card .card-top{
  color: #6f6b80;
  font-weight: 300;
  line-height:26px;
}
.card .card-title{
  color: hsl(247, 35%, 19%);
  font-weight: 700;
  font-size: 24px;
}
.card .card-title:hover{
  color: #525EE0;
  cursor:pointer;
}
.card-footer{
  border-top: solid 1px rgba(255, 254, 254, 0.75);
  padding: 32px;
  display:flex;
  justify-content: space-between;
}

.card-footer .salary  .old{
  color: hsl(251, 9%, 46%);
  font-weight: 400;
  margin-left: 4px;
  text-decoration: line-through;

}
.card-footer .salary  .new{
  color: #525ee0;
  font-size:18px;
}
.card-footer .students  span{
  font-weight: 400;
  font-size: 17px;
  margin-left: 6px;
  color: hsl(251, 9%, 46%);
}

</style>
