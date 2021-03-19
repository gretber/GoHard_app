<template>
  <div class="our_services_heading__container">
    <h2 class="our_services_heading">
      <span> Our </span>
      Services
    </h2>
  </div>
</template>
<style scoped>
.our_services_heading__container{
  width: 100%;
  min-height: 100vh;
  display: flex;
  justify-content: center;
  align-items: center;
  background-image: url(@/assets/ourServices/bg_our_services.jpg);
  background-repeat: no-repeat;
  background-position: center;
  background-size: cover;
}

.our_services_heading{
  color: #228A43;
  font-size: 100px;
}
span{
  color: #FFFFFF;
}
@media screen and (max-width: 620px){
  .our_services_heading{
    font-size: 60px;
  }
  span:before{
    bottom: 5px;
  }
}
@media screen and (max-width: 400px){
  .our_services_heading{
    font-size: 45px;
  }
}
</style>
