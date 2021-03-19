<template>
  <div class="our_services__content">
    <div class="our_services__content__container">
      <p class="our_services__description">
        We are a fast-growing software development agency with a strong expertise in the most relevant and innovative programming languages, frameworks, libraries and tools. We
        are a fast-growing software development agency with a strong expertise in the
        most relevant and innovative programming languages, frameworks,
        libraries and tools.
      </p>
      <div class="our_services__blocks">
        <div v-for="(block, index) of blocks" :key="index" class="block" :class="block.class">
          <div class="caption">
            <div class="caption__number">
              <img :src="block.src" alt="block image">
            </div>
            <div class="caption__description">
              <div class="heading-green">
                {{ block.heading_1 }}
              </div>
              {{ block.heading_2 }}
            </div>
          </div>
          <div class="description">
            {{ block.description }}
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
        { class: 'left', src: require('../../assets/main/services/web_dev.gif'), heading_1: 'Web', heading_2: 'Development', description: 'We are always ready to discuss your request and find the best solutions for your case. Also, one of our developers could be a part of your team on one of the existing projects as an outstaff member.' },
        { class: 'right', src: require('../../assets/main/services/mobile_develop.gif'), heading_1: 'Mobile', heading_2: 'Development', description: 'Our stack covers Android Native, iOS Native and Cross-platform development. Depending on your idea, business objectives and requirements we will estimate, discover and implement the project in the most relevant way to provide each case with the expected quality and result.' },
        { class: 'left', src: require('../../assets/main/services/design.gif'), heading_1: 'UI/UX', heading_2: 'Design', description: 'Our experienced and creative designers are always looking for a possibility to use their inspiration to achieve the desired result, why not on your project?' },
        { class: 'right', src: require('../../assets/main/services/legacy.gif'), heading_1: 'Legacy Code', heading_2: 'Redevelopment', description: 'Have an existing project and would like to update it? Would be great to find the best solution for you, according to the most innovative technologies and tools.' },
        { class: 'left', src: require('../../assets/main/services/consulting.gif'), heading_1: 'Consulting', heading_2: 'Estimation', description: 'Have a project and a team of developers? We could estimate and consult about the best technologies stack. In order to make you be sure you are provided with the best possible solution.' },
        { class: 'right', src: require('../../assets/main/services/code_review.gif'), heading_1: 'Code', heading_2: 'Review', description: 'Have a project and a team of developers? We could estimate and consult about the best technologies stack. In order to make you be sure you are provided with the best possible solution.' },
        { class: 'left', src: require('../../assets/main/services/sofware.gif'), heading_1: 'Software', heading_2: 'Maintenance', description: 'We are always ready to support and advise your project after the development process is finished.' },
        { class: 'right', src: require('../../assets/main/services/product_develop.gif'), heading_1: 'Product', heading_2: 'Develop', description: 'Previous experience in creating an idea, development and support of different solutions in the Medical and Telecommunication fields gives us a quite deep understanding of business processes and the ways of solving issues. That’s why our product managers can provide you with some advice for further improvements.' }
      ]
    }
  }
}
</script>
<style scoped>
.our_services__content{
  width: 100%;
  height: 100%;
  display: flex;
  justify-content: center;
  align-items: center;
}
.our_services__content__container{
  width: 1100px;
  padding: 50px 25px;
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
}
.our_services__description{
  text-align: center;
  font-size: 23px;
  color: #A5A5A5;
  max-width: 750px;
}
.our_services__blocks{
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: flex-start;
}
.our_services__blocks:first-child{
  background-color: red;
}
.block{
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
}
.heading-green{
  color: #228A43;
}
.caption__description{
  text-align: center;
  font-size: 24px;
  font-weight: 700;
  color: #fff;
}
.description{
  padding: 25px;
  width: 100%;
  color: #A5A5A5;
  font-size: 18px;
  text-align: center;
  display: flex;
  justify-content: center;
  align-items: center;
}
.left {
  margin: 25px 300px 25px 0;
}
.right{
  margin: 25px 0 25px 300px;
}

@media screen and (max-width: 1100px){
  .our_services__content__container{
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
@media screen and (max-width: 620px){
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
