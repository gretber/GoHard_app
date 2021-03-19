<template>
  <section class="main__portfolio">
    <div class="main__portfolio__container">
      <div class="header">
        Portfolio
      </div>
      <div class="portfolio__description">
        Here are some of our previous projects that we worked on and implemented customers requirements and ideas,
        in order to achieve their business objectives.
      </div>
      <el-carousel class="carousel" :interval="4000" type="card">
        <el-carousel-item v-for="(item, index) in sliderImages" :key="index">
          <h3 class="medium" :style="{ backgroundImage: 'url(' + item.src + ')' }">
            <!-- {{ item.description }}-->
          </h3>
        </el-carousel-item>
      </el-carousel>
      <button class="our__works__button">
        Our works
      </button>
    </div>
  </section>
</template>
<script>
export default {
  data () {
    return {
      sliderImages: [
        { description: 'Web development', src: require('../../assets/main/slider/1.jpg') },
        { description: 'Web development', src: require('../../assets/main/slider/2.jpg') },
        { description: 'Web development', src: require('../../assets/main/slider/1.jpg') },
        { description: 'Web development', src: require('../../assets/main/slider/2.jpg') }
      ]
    }
  },
  methods: {
  }
}
</script>

<style scoped>
  .main__portfolio{
    width: 100%;
    display: flex;
    justify-content: center;
    align-items: center;
  }
  .main__portfolio__container{
    display: flex;
    flex-direction: column;
    justify-content: flex-start;
    align-items: center;
    width: 1100px;
    height: 100%;
    padding: 100px 0;
  }
  .header{
    font-weight: 400;
    font-size: 35px;
    color: #228A43;
    border-bottom: 1px solid #228A43;
  }
  .portfolio__description{
    margin-top: 50px;
    font-weight: 300;
    font-size: 23px;
    text-align: center;
    line-height: 31px;
    color: #A5A5A5;
  }
  .our__works__button{
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
  .our__works__button:hover{
    background-color: #228A43;
  }
  .carousel{
    margin: 50px 0 0 0;
    width: 1100px;
  }
  .medium{
    background-color: black;
    opacity: 0.3;
    background-repeat: no-repeat;
    background-size: cover;
    margin: 0;
    width: 100%;
    height: 100%;
    border-radius: 15px;
    transition: all 0.3s;
  }
  .el-carousel__item--card.is-active .medium{
    opacity: 1!important;
  }
  .el-carousel__item:nth-child(2n) {
    background-color: black;
  }

  .el-carousel__item:nth-child(2n+1) {
    background-color: black;
  }
  @media screen and (max-width: 1100px){
    .main__portfolio__container{
      padding: 25px;
      width: 100%;
    }
    .carousel{
      width: 100%;
    }
  }
</style>
<style>
.el-carousel__indicator--horizontal button{
  background-color: #228A43!important;
  opacity: 0.5;
}
</style>
