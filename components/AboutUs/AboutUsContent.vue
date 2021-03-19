<template>
  <div class="about_us__content">
    <div class="about_us__content__container">
      <h2 class="heading">Why Us?</h2>
      <p class="about_us__description">
        Working about 2 years on the market, we consider us as a fast-growing and developing software development agency. We spent a lot of time building a team of experienced developers/designers, in order to discover new horizons in the quality of customers services.
      </p>
      <div class="about_us__blocks">
        <div class="block" v-for="(block, index) of blocks" :key="index" :class="block.class">
          <div class="caption">
            <div class="caption__number">
              {{block.number}}
            </div>
            <div class="caption__description">
              {{block.heading}}
            </div>
          </div>
          <div class="description">
            {{block.description}}
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
      blocks: [
        { class: 'left', number: 7, heading: 'Most relevant programming languages', description: 'We are always aware of the most innovative and relevant technologies, in order to make our projects comfortable and convenient to update and develop in future. We focus on JavaScript, Python, PHP(Modern), Golang, React Native, Kotlin, Swift' },
        { class: 'right', number: 4, heading: 'Fields of business we work with', description: 'Most of our previous projects are related to medical, delivery, educational and construction industries.' },
        { class: 'left', number: 2, heading: 'Years of software development at the market', description: 'Working about 2 years on the market, we consider us as a fast-growing and developing software development agency. We spent a lot of time building a team of experienced developers/designers, in order to discover new horizons in the quality of customers services.' },
        { class: 'right', number: 1, heading: 'Strong team of professionals', description: 'Despite the fact that a part of our developers work in office and others work on a remote positions, we are one team of united professionals who works as one tool.' }
      ]
    }
  }
}
</script>
<style scoped>
  .about_us__content{
    width: 100%;
    height: 100%;
    display: flex;
    justify-content: center;
    align-items: center;
  }
  .about_us__content__container{
    width: 1100px;
    padding: 50px 25px;
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
  }
  .heading{
    color: #228A43;
    font-size: 50px;
    font-weight: bold;
  }
  .about_us__description{
    text-align: center;
    font-size: 23px;
    color: #A5A5A5;
    max-width: 850px;
  }
  .about_us__blocks{
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: flex-start;
  }
  .block{
    box-sizing: border-box;
    padding: 5px;
    border-radius: 5px;
    width: 750px;
    height: 250px;
    border: 1px solid #a5a5a5;
    backdrop-filter: blur(26px);
    display: flex;
    box-shadow: 0px 0px 44px rgba(34, 138, 67, 0.35);
  }
  .caption{
    padding: 5px;
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
    flex-wrap: wrap;
    width: 350px;
    height: 100%;
    color: #228A43;
    box-sizing: border-box;
  }
  .caption__number{
    font-size: 96px;
    line-height: 130px;
    text-align: center;
    font-weight: 500;
  }
  .caption__description{
    text-align: center;
    font-size: 22px;
    color: #fff;
    font-weight: bold;
  }
  .description{
    padding: 25px;
    width: 100%;
    color: #A5A5A5;
    font-size: 22px;
    text-align: center;
    display: flex;
    justify-content: center;
    align-items: center;
  }
  .left{
    margin: 25px 300px 25px 0;
  }
  .right{
    margin: 25px 0 25px 300px;
  }
  @media screen and (max-width: 1100px){
    .about_us__content__container{
      width: 100%;
      padding: 25px;
    }
    .block{
      margin: 25px 0;
    }
  }
  @media screen and (max-width: 800px){
    .block{
      width: 100%;
      height: auto;
    }
  }
  @media screen and (max-width: 700px){
    .block{
      flex-direction: column;
      height: auto;
    }
    .caption{
      width: 100%;
    }
    .description{
      width: auto;
    }
  }
</style>
