<template>
  <div class="courses">
    <div class="container">
      <div class="courses-text text-center">
        <div class="subtitle">
          COURSE CATEGORIES
        </div>
        <div class="title">
          Popular Topics To Learn
        </div>
      </div>
      <div class="row">

        <div class="col-lg-4 col-sm-12 col-md-6 mt-5" v-for="card in cards" :key="card">
          <div class="card courses-card">
            <div class="card-content">
              <div class="card-body">
                <div class="media d-flex gap-5">
                  <div class="align-self-center fa-2x course-icon ">
                    <fa :icon="card.icon" class="stroke-transparent"/>
                </div>
                <div class="media-body text-right">
                  <h3 class="course-title"> {{ card.title }} </h3>
                  <span class="course-txt"> {{ card.txt }}</span>
                </div>
              </div>
            </div>
          </div>
        </div>
        </div>
      </div>
    </div>
  </div>

  <!--
    fa-briefcase
    fa-briefcase-medical
    fa-database
    fa-headphones-alt
    fa-laptop
    fa-layer-group
    fa-wallet
    fa-pencil
    fa-thumbs-up
   -->
</template>

<script>
export default {
  data () {
    return {
      cards: [
        {
          id: 1,
          title: ' Development',
          txt: '39 Course',
          icon: 'fa-briefcase'
        },
        {
          id: 2,
          title: 'Human Research',
          txt: '24 Course',
          icon: 'fa-search'
        },
        {
          id: 3,
          title: 'Art & Design',
          txt: '39 Course',
          icon: 'fa-pencil'
        },
        {
          id: 4,
          title: ' Management',
          txt: '39 Course',
          icon: 'fa-database'
        },
        {
          id: 5,
          title: 'Web Development',
          txt: '39 Course',
          icon: 'fa-laptop'
        },
        {
          id: 6,
          title: 'LifeStyle',
          txt: '12 Course',
          icon: 'fa-thumbs-up'
        },
        {
          id: 7,
          title: 'Digital Marketing',
          txt: '39 Course',
          icon: 'fa-headphones-alt'
        },
        {
          id: 8,
          title: 'Data Sciences',
          txt: '39 Course',
          icon: 'fa-database'
        },
        {
          id: 9,
          title: 'Health & Fitness',
          txt: '39 Course',
          icon: 'fa-laptop'
        }

      ]
    }
  }
}
</script>

<style>
.courses{
  width: 100%;
  padding-top: 180px;
  height: fit-content;
  background-size:cover;
  padding-block: 80px;
  padding-block-start:100px;
}
.stroke-transparent{
   -webkit-text-stroke: 1px #000;
 -webkit-text-fill-color: transparent;
}
.courses-card{
  background: hsl(0, 0%, 96%);
  border: none;
  border-radius: 6px;
  padding-inline:10px;
  padding: 5px;
  transition:0.25s ease;
}
.courses-card .course-icon{
  color: hsl(235, 70%, 60%);
  height: 60px;
  min-width: 60px;
  background-color:white;
  display:grid;
  place-items:center;
}
.course-title {
  font-size: 22px;
  color: hsl(247, 35%, 19%);
  font-weight: 600;
}
.course-txt{
  color: #6f6b80;
  font-size: 16px;
}
  .courses-card:hover{
    background:hsl(235, 70%, 60%);
    color:white;
    cursor: pointer;
  }
  .courses-card:hover .course-txt ,
  .courses-card:hover .course-title  {
    color:white;
  }
  .courses-card:hover .course-icon {
    background-color:hsla(0, 0%, 100%, 0.1);
    color: white;
  }
</style>
