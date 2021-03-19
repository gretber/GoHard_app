<template>
  <section class="about__us">
    <div class="about__us__container">
      <div class="about__us__left__container">
        <h2 class="head">
          <span class="head__about">About</span>
          us
        </h2>
        <div class="left__container__content">
          We are a fast-growing software development
          company with a strong expertise in the most
          relevant and innovative programming
          languages, frameworks, libraries
          and tools.
        </div>
        <nuxt-link to="/about-us" tag="button" class="left__container__button">
          Read more
        </nuxt-link>
      </div>
      <div class="about__us__right__container">
        <div class="right__container__box container-first">
          <span class="box__number">7</span>
          <span class="box__text">Most relevant programming languages</span>
        </div>
        <div class="right__container__box container-second">
          <span class="box__number">4</span>
          <span class="box__text"> Fields of business we work with</span>
        </div>
        <div class="right__container__box container-third">
          <span class="box__number">2</span>
          <span class="box__text">Years of software development at the market</span>
        </div>
        <div class="right__container__box container-fourth">
          <span class="box__number">1</span>
          <span class="box__text">Strong team of professionals</span>
        </div>
      </div>
      <nuxt-link tag="button" to="/about-us" class="mobile__button">
        More
      </nuxt-link>
    </div>
  </section>
</template>
<style scoped>
  .about__us{
    width: 100%;
    height: 510px;
    background-image: url(@/assets/main/bg_about.jpg);
    box-shadow: 0 0 10px rgba(245, 245, 245, 0.3);
    border-radius: 10px;
    display: flex;
    justify-content: center;
  }
  .about__us__container{
    width: 1100px;
    height: 100%;
    display: flex;
    justify-content: space-between;
  }
  .about__us__left__container{
    margin-right: 15px;
    padding: 0 0;
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: flex-start;
    width: 50%;
  }
  .head{
    font-weight: 400;
    font-size: 35px;
    color: #fff;
  }
  .head__about{
    color: #228A43;
    border-bottom: 1px solid #228A43;
  }
  .left__container__content{
    margin-top: 15px;
    color: #A5A5A5;
    font-size: 23px;
    line-height: 34px;
    font-weight: 400;
  }
  .left__container__button{
    margin-top: 40px;
    width: 220px;
    height: 50px;
    background: rgba(255, 255, 255, 0.01);
    border: 1px solid #228A43;
    backdrop-filter: blur(10px);
    border-radius: 5px;
    color: #fff;
    font-size: 20px;
    outline: none;
    transition: all 0.3s;
    cursor: pointer;
    font-weight: bold;
  }
  .left__container__button:hover{
    background-color: #228A43;
  }
  .about__us__right__container{
    width: 50%;
    display: flex;
    justify-content: center;
    align-items: center;
  }
  .right__container__box{
    width: 140px;
    height: 150px;
    border: 1px solid #FFFFFF;
    border-radius: 5px;
    backdrop-filter: blur(26px);
    background: rgba(255, 255, 255, 0.01);
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
    color: #fff;
    box-sizing: border-box;
    transition: all 0.3s;
    margin: 0px 3px;
    padding: 0px 5px;
  }
  .container-first{
    margin-bottom: 100px;
  }
  .container-third{
    margin-top: 100px;
  }
  .container-fourth{
    margin-top: 200px;
  }
  .box__number{
    font-size: 70px;
    font-weight: 400;
  }
  .box__text{
    font-size: 14px;
    text-align: center;
    margin-bottom: 15px;
  }
  .right__container__box:hover{
    color: #228A43;
    border: 1px solid #228A43;
  }
  .mobile__button{
    display: none;
  }
  @media screen and (max-width: 1100px){
    .left__container__button{
      display: none;
    }
    .about__us{
      height: 100%;
      background-repeat: no-repeat;
      background-position: center;
      background-size: cover;
      padding: 50px 0;
    }
    .about__us__container{
      padding: 0 25px;
      flex-direction: column;
      justify-content: center;
      align-items: center;
    }
    .about__us__left__container{
      width: 80%;
      align-items: center;
    }
    .left__container__content{
      text-align: center;
      font-size: 23px;
    }
    .about__us__right__container{
      width: 100%;
      flex-wrap: wrap;
    }
    .right__container__box{
      margin: 20px 5px;
    }
    .mobile__button{
      display: block;
      margin-top: 40px;
      width: 220px;
      height: 50px;
      background: rgba(255, 255, 255, 0.01);
      border: 1px solid #228A43;
      backdrop-filter: blur(10px);
      border-radius: 5px;
      color: #fff;
      font-size: 20px;
      outline: none;
      transition: all 0.3s;
      cursor: pointer;
      font-weight: bold;
    }
    .mobile__button:hover{
      background-color: #228A43;
    }
  }
</style>
