<template>
  <section class="our__services">
    <div class="our__-services__container">
      <div class="header">
        Our
        <span class="header_services">services</span>
      </div>
      <div class="services__blocks">
        <el-row>
          <el-col
            v-for="(block, index) of blocks"
            :key="index"
            :xs="12"
            :sm="8"
            :md="6"
            class="services_block__container"
          >
            <div class="services_block">
              <img :src="block.src" alt="block image">
              <div class="description">
                {{ block.description }}
              </div>
            </div>
          </el-col>
        </el-row>
      </div>
      <div class="services_description">
        Based on our previous expertise in Web/Mobile development, experience with a Product solutions and Design, we are always doing our best to provide you with the expected results.
      </div>
      <nuxt-link tag="button" to="/our-services" class="services__button">
        More details
      </nuxt-link>
    </div>
  </section>
</template>
<script>
export default {
  data () {
    return {
      blocks: [
        { description: 'Web development', src: require('../../assets/main/services/web_dev.gif') },
        { description: 'Mobile development', src: require('../../assets/main/services/mobile_develop.gif') },
        { description: 'UI/UX design', src: require('../../assets/main/services/design.gif') },
        { description: 'Legacy Code Redevelopment', src: require('../../assets/main/services/legacy.gif') },
        { description: 'Consulting/Estimation', src: require('../../assets/main/services/consulting.gif') },
        { description: 'Code Review', src: require('../../assets/main/services/code_review.gif') },
        { description: 'Software Maintenance', src: require('../../assets/main/services/sofware.gif') },
        { description: 'Product development and support', src: require('../../assets/main/services/product_develop.gif') }
      ]
    }
  }
}
</script>
<style scoped>
  .our__services{
    width: 100%;
    padding: 100px 0px;
    display: flex;
    justify-content: center;
    align-items: center;
  }
  .our__-services__container{
    padding: 10px;
    display: flex;
    flex-direction: column;
    justify-content: flex-start;
    align-items: center;
    width: 1100px;
    height: 100%;
  }
  .header{
    font-weight: 400;
    font-size: 35px;
    color: #fff;
  }
  .header_services{
    color: #228A43;
    border-bottom: 1px solid #228A43;
  }
  .services__blocks{
    width: 100%;
    margin-top: 50px;
  }
  .services_block__container{
    display: flex;
    justify-content: center;
    align-items: center;
  }
  .services_block{
    margin-top: 25px;
    box-sizing: border-box;
    width: 180px;
    height: 155px;
    display: flex;
    flex-direction: column;
    justify-content: flex-start;
    align-items: center;
  }
  .description{
    margin-top: 15px;
    color: #fff;
    text-align: center;
    font-size: 18px;
  }
  .services_description{
    max-width: 920px;
    text-align: center;
    font-weight: 300;
    font-size: 23px;
    line-height: 31px;
    color: #A5A5A5;
  }
  .services__button{
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
  .services__button:hover{
    background-color: #228A43;
  }
  @media screen and (max-width: 440px) {
    .description{
      font-size: 14px;
    }
  }
</style>
