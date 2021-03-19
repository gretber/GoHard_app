<template>
  <div class="portfolio__container">
    <h2 class="portfolio__heading">
      Portfolio
    </h2>
  </div>
</template>
<style scoped>
.portfolio__container{
  width: 100%;
  min-height: 100vh;
  display: flex;
  justify-content: center;
  align-items: center;
  background-image: url(@/assets/portfolio/header_bg.jpg);
  background-repeat: no-repeat;
  background-position: center;
  background-size: cover;
}
.portfolio__heading{
  color: #228A43;
  font-size: 100px;
}
span{
  color: #FFFFFF;
}
@media screen and (max-width: 520px){
  .portfolio__heading{
    font-size: 40px;
  }
  span:before{
    bottom: 5px;
  }
}
</style>
