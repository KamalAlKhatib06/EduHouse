<template>
  <div class="events" id="event">
    <div class="container">
        <div class="content text-center">
            <div class="subtitle">UPCOMMING EVENT</div>
            <div class="title">Let’s Join Our Community</div>
        </div>
        <div class="row">
            <div class="col-lg-4 col-md-6 col-sm-12" v-for="event in events" :key="event.id">
                <div class="card mt-5 border-0 ">
                    <div class="card-banner">
                        <div class="card-banner-text">
                            {{ event.time }}
                        </div>
                        <img class="card-img img-fluid" :src="require(`../assets/event-${event.id}.jpg`)" />
                    </div>
                    <div class="card-body card-top">
                        <p class="text-black-50">
                            <fa icon="fa-solid fa-location-arrow" />
                            {{ event.place }}
                        </p>
                        <div class="card-title">
                            {{ event.title }}
                        </div>
                        <div class="event-hover">
                            Get Ticket
                            <fa icon="fa-solid fa-arrow-right-long mx-1" class="px-2"></fa>
                        </div>
                    </div>
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
      events: [
        {
          id: 1,
          time: '04 Dec 2022',
          place: 'Alpaca Way Anaheim, CA 92805',
          title: 'Innovation & Technological Enterpreneurship Team',
          img: '../assets/event-1.jpg'
        },
        {
          id: 2,
          time: '30th Oct 2022',
          place: 'Ritter Avenue Detroit, MI 48226',
          title: 'Virtual Spring Part-time Jobs Fair For Students',
          img: '../assets/event-2.jpg'
        },
        {
          id: 3,
          time: '18th Sep 2022',
          place: 'Stout Street York, PA 17401',
          title: 'Exploration of Regional Chief Executive Network',
          img: '../assets/event-3.jpg'
        }
      ]
    }
  }
}
</script>

<style scoped>
.events{
    width: 100%;
    padding-top: 180px;
    height: fit-content;
    background-size:cover;
    padding-block: 80px;
    padding-block-start:100px;
}
.card{
    background: #eee;
    font-family:Urbanist;
}
.card-banner{
    position: relative;
}
.card-banner-text{
    position: absolute;
    top: 20px;
    /* left:20px; */
    border-top-right-radius: 12px;
    border-bottom-right-radius:12px ;
    width: 120px;
    font-weight: 700;
    text-align:center;
    background:#525ee0;
    color:white;
    font-family:Urbanist;
    padding: 5px;
}
.card .card-title{
    color: hsl(247, 35%, 19%);
    font-weight: 700;
    font-size:24px;
    font-family:Urbanist;
    line-height: 36px;
}
.card .card-title:hover{
    color:#525ee0;
    cursor:pointer;
}
.event-hover{

    background:
       linear-gradient(currentColor 0 0) left  var(--p, 50%) bottom 0 /var(--d, 10%) 3px no-repeat,
       linear-gradient(currentColor 0 0) right var(--p, 50%) bottom 0 /var(--d, 10%) 3px no-repeat;
    transition: 0.3s, background-position 0.3s 0.3s;
    color: #525ee0;
    font-weight: 600;
    line-height: 48px;
    font-family:Urbanist;
    width: fit-content;
}
.event-hover:hover{
  --d: 100%;
  --p: 100%;
  cursor:pointer;
  transition: 0.3s, background-size 0.3s 0.3s;

}

</style>
