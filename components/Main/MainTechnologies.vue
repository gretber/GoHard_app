<template>
  <section class="technologies">
    <div class="technologies__container">
      <img src="@/assets/main/technologies/image_tech.svg" alt="notebook">
      <div class="technologies__container__info">
        <h2 class="info__heading">
          Technologies
        </h2>
        <div class="info__description">
          In our work we always focus on the most flexible, innovative and relevant
          programming languages, frameworks and libraries.
        </div>
        <nuxt-link tag="button" to="/technologies" class="info__button">
          Watch list
        </nuxt-link>
      </div>
    </div>
  </section>
</template>
<style scoped>
  .technologies{
    width: 100%;
    min-height: 500px;
    background-image: url(@/assets/main/technologies/bg_tech.jpg);
    display: flex;
    justify-content: center;
    align-items: center;
  }
  .technologies__container{
    width: 1100px;
    height: 100%;
    display: flex;
    justify-content: center;
    align-items: center;
  }
  .technologies__container__info{
    width: 50%;
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: flex-end;
  }
  .info__heading{
    color: #228A43;
    font-size: 25px;
    line-height: 47px;
    font-weight: 400;
    border-bottom: 1px solid #228A43;
  }
  .info__description{
    margin-top: 25px;
    max-width: 465px;
    font-size: 23px;
    color: #A5A5A5;
    font-weight: 300;
    line-height: 31px;
    text-align:right;
  }
  .info__button{
    margin-top: 80px;
    width: 220px;
    height: 50px;
    background: rgba(255, 255, 255, 0.01);
    border: 1px solid #228A43;
    backdrop-filter: blur(10px);
    border-radius: 5px;
    color: #fff;
    font-size: 18px;
    transition: all 0.3s;
    font-weight: bold;
    cursor: pointer;
  }
  .info__button:hover{
    background-color: #228A43;
  }
  @media screen and (max-width: 1100px){
    .technologies__container{
      width: 100%;
      padding: 15px;
      flex-direction: column;
    }
    .technologies__container__info{
      align-items: center;
      width: 100%;
    }
    .info__description{
      text-align: center;
    }
  }
  @media screen and (max-width: 610px){
    img{
      width: 100%;
    }
  }
</style>
