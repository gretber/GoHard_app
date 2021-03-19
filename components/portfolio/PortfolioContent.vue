<template>
  <div class="portfolio_content">
    <div class="portfolio_container">
      <h2 class="heading">
        Our works
      </h2>
      <div class="portfoio_description">
        Here are some of our most relevant and challenging projects that we worked with and implemented customers requirements and ideas, in order to achieve their business objectives.
      </div>
      <el-carousel :interval="4000" indicator-position="none" height="450px">
        <el-carousel-item v-for="(slide, index) of blocks" :key="index">
          <div class="carousel_item" :style='{ backgroundImage: "url(" + slide.backgroung + ")", }'>
            <div class="carousel_description">
              <div class="content">
                <div class="content__heading">
                  {{ slide.heading }}
                </div>
                <div class="content__description">
                  {{ slide.description }}
                </div>
              </div>
              <div class="technologies">
                <div class="technologies__heading">
                  Technologies:
                </div>
                <div class="technologies__images">
                  <img v-for="(img, imgIndex) in slide.technolofies" :key="imgIndex" :src="img.src" alt="">
                </div>
              </div>
            </div>
          </div>
        </el-carousel-item>
      </el-carousel>
    </div>
  </div>
</template>
<script>
export default {
  data () {
    return {
      blocks: [
        {
          heading: 'Medical equipment website',
          description: 'The task was to create working website for current company with all of their equipment and warehouses. The client was fully satisfied.',
          backgroung: require('../../assets/portfolio/slider/first/background.png'),
          technolofies: [
            { src: require('../../assets/portfolio/slider/first/technologies/html.png') },
            { src: require('../../assets/portfolio/slider/first/technologies/css 1.png') },
            { src: require('../../assets/portfolio/slider/first/technologies/js 1.png') },
            { src: require('../../assets/portfolio/slider/first/technologies/Vector.png') }
          ]
        }
      ]
    }
  }
}
</script>
<style>
.el-carousel--horizontal{
  margin-top: 50px;
  width: 100%;
  height: 600px;
  padding: 15px;
}

.carousel_item{
  height: 100%;
  position: relative;
  border-radius: 15px;
  background-size: cover;
  background-repeat: no-repeat;
}
.carousel_description{
  position: absolute;
  left: 0;
  right: 0;
  bottom: 0;
  height: 160px;
  background-color: rgba(0,0,0, 1);
  display: flex;
  justify-content: center;
  align-items: center;
  border-radius: 0 0 15px 15px;
}
.content{
  color: #fff;
  display: flex;
  flex-direction: column;
  justify-content: flex-start;
  align-items: flex-start;
  width: 65%;
  padding: 25px;
}
.content__description{
  margin-top: 15px;
  font-size: 18px;
  color: #a5a5a5;
}
.content__heading{
  font-size: 30px;
  line-height: 34px;
  font-weight: 400;
}
.technologies{
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
  width: 35%;
  height: 100%;
  padding: 0 15px;
}
.technologies__heading{
  font-size: 28px;
  color: #FFFFFF;
  font-weight: 400;
}
.technologies__images{
  margin-top: 15px;
  display: flex;
  justify-content: center;
  align-items: center;
}
.technologies__images img {
  width: 40px;
  height: 40px;
  margin: 0 15px;
}

.portfolio_content{
  width: 100%;
  height: 100%;
  display: flex;
  justify-content: center;
  align-items: center;
}
.portfolio_container{
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
.portfoio_description{
  text-align: center;
  font-size: 23px;
  color: #A5A5A5;
  max-width: 850px;
}
@media screen and (max-width: 1100px){
  .portfolio_container{
    width: 100%;
    padding: 25px;
  }

}
@media screen and (max-width: 700px){
  .portfoio_description{
    width: auto;
  }
}
</style>
<style>
.el-carousel__container{
  border-radius: 15px;
  box-shadow: 0px 0px 11.6221px rgba(255, 255, 255, 0.25);
}
</style>
