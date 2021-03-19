<template>
  <div class="about__us__heading__container">
    <h2 class="about__us__heading">
      Technologies
    </h2>
  </div>
</template>
<style scoped>
.about__us__heading__container{
  width: 100%;
  min-height: 100vh;
  display: flex;
  justify-content: center;
  align-items: center;
  position: relative;
}
.about__us__heading__container:after{
  content: "";
  opacity: 0.3;
  top: 0;
  left: 0;
  bottom: 0;
  right: 0;
  position: absolute;
  z-index: -1;
  background-image: url(@/assets/technologies/head_bg.gif);
  background-repeat: no-repeat;
  background-position: center;
  background-size: cover;
}
.about__us__heading{
  color: #228A43;
  font-size: 100px;
}
span{
  color: #FFFFFF;
}
@media screen and (max-width: 670px){
  .about__us__heading{
    font-size: 60px;
  }
  span:before{
    bottom: 5px;
  }
}
@media screen and (max-width: 400px) {
  .about__us__heading {
    font-size: 42px;
  }
}
</style>
