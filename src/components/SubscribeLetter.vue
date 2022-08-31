<template>
  <div class="sub" id="sub">
    <div class="container">
      <div class="content text-center">
        <div class="subtitle">
          SUBSCRIBE NEWSLETTER
        </div>
        <div class="title">
          Get Every Latest News
        </div>

          <div class="sub-form ">
            <input type="email" class="sub-inp mt-5" placeholder="Enter Your Email">
            <div class="inp-wrapper">
              <div class="sub-icon mt-5">
                <fa icon="fa-solid fa-house" />
              </div>
              <button class="btn sub-btn d-flex mt-5">
                Subscribe
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

}
</script>

<style scoped>
.sub{
  width: 100%;
  padding-top: 180px;
  height: fit-content;
  background-size:cover;
  padding-block: 80px;
  background:#F8E9E2;
  padding-block-start:100px;
}
.sub-form{
  padding: 10px;
  position: relative;
}
.sub-inp{
  height: 80px;
  padding-inline: 45px 20px;
  border-radius:12px ;
  margin-block-end:20px;
  width: 100%;
  color: #111;
  border: none;
  font-family:Urbanist;
}
.sub-inp:focus{
  outline: none;
  border:none;
}
.sub-inp::placeholder{
  font-family:Urbanist;
}
.inp-wrapper{
  displaY:flex;
  justify-content:space-between;
  top: 20%;
  gap: 100px;
}
.sub-btn{
  position:absolute;
  top:12%;
  right: 25px;
  bottom:50%;
  font-weight: 600;
  padding-inline:35px;
  min-height: 60px;
  font-family: Urbanist;
  letter-spacing:1px;
  max-width: max-content;
  display: flex;
  align-items: center;
  gap: 10px;
  background: #525ee0;
  color:white;
  border-radius: 6px;
  transition: .25 ease;
}
@media(max-width:460px){
  .sub-btn{
    padding-inline:0;
    padding: 6px;
  }
}
.sub-btn:hover, .sub-btn:focus{
  background: hsl(247, 35%, 19%);
  color:white;
  box-shadow: none;
}
.sub-icon{
  position: absolute;
  top: 22%;
  /* transform:translateY(10%); */
  left: 25px;
  color: #525ee0;
  /* top: 15%;
  bottom: 50%;*/
}
</style>
