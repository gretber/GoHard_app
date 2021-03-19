<template>
  <div class="technologies__content">
    <div class="technologies__container">
      <div v-for="(block, index) of blocks" :key="index">
        <div class="slider__container">
          <div class="slider__heading">
            <span class="head_1">{{ block.head_1 }}</span> {{ block.head_2 }}
          </div>
          <div class="slider__description">
            {{ block.description }}
          </div>
          <el-carousel :interval="2000" indicator-position="none" height="400px" type="card">
            <el-carousel-item v-for="(item, item_index) in block.slides" :key="item_index">
              <img class="carousel--img" :src="item.img" alt="js">
              <div class="carousel--heading">
                {{ item.head }}
              </div>
              <div class="carousel--description">
                {{ item.description }}
              </div>
            </el-carousel-item>
          </el-carousel>
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
        {
          head_1: 'Front-end',
          head_2: 'development',
          description: 'Front-end is the brightest showcase how your website can look and felt by users. User friendly design and functionality makes the difference in the way how users perceive the information.',
          slides: [
            {
              img: require('../../assets/technologies/Front/js.png'),
              head: 'JS',
              description: 'JavaScript is a lightweight, interpreted, or just-in-time compiled programming language with first-class functions.'
            },
            {
              img: require('../../assets/technologies/Front/react.png'),
              head: 'React.js',
              description: 'React makes it painless to create interactive UIs.'
            },
            {
              img: require('../../assets/technologies/Front/vue.png'),
              head: 'Vue.js',
              description: 'Vue is a progressive framework for building user interfaces. Unlike other monolithic frameworks, Vue is designed from the ground up to be incrementally adoptable.'
            },
            {
              img: require('../../assets/technologies/Front/html.png'),
              head: 'HTML',
              description: 'HTML is the standard markup language for Web pages.'
            },
            {
              img: require('../../assets/technologies/Front/css.png'),
              head: 'CSS',
              description: 'CSS describes how HTML elements are to be displayed.'
            },
            {
              img: require('../../assets/technologies/Front/bootstrap.png'),
              head: 'Bootstrap',
              description: 'Quickly design and customize responsive mobile-first sites with Bootstrap.'
            },
            {
              img: require('../../assets/technologies/Front/material.png'),
              head: 'Material-UI',
              description: 'React component for faster and easier web development.'
            },
            {
              img: require('../../assets/technologies/Front/elements.png'),
              head: 'Element',
              description: 'Element, a Vue 2.0 based component library for developers, designers and product managers'
            },
            {
              img: require('../../assets/technologies/Front/nuxt.png'),
              head: 'Nuxt.js',
              description: 'An open source framework making web development simple and powerful.'
            },
            {
              img: require('../../assets/technologies/Front/next.png'),
              head: 'Next.js',
              description: 'Next.js gives you the best developer experience with all the features you need for production: hybrid static & server rendering.'
            }
          ]
        },
        {
          head_1: 'Back-end',
          head_2: 'development',
          description: 'Quality of back-end on your project is a direct characteristic of the quality of the project. That is why the right choice of technologies used, is so important.',
          slides: [
            {
              img: require('../../assets/technologies/back/js.png'),
              head: 'JS',
              description: 'Lorem ipsum dolor sit amet, consectetur adipiscing elit. Lacus, nisl, lectus nisl sed quis non. Eget porta elit sit tempor eu sit.'
            },
            {
              img: require('../../assets/technologies/back/node.png'),
              head: 'Node.js',
              description: 'Lorem ipsum dolor sit amet, consectetur adipiscing elit. Lacus, nisl, lectus nisl sed quis non. Eget porta elit sit tempor eu sit.'
            },
            {
              img: require('../../assets/technologies/back/express.png'),
              head: 'Express.js',
              description: 'Lorem ipsum dolor sit amet, consectetur adipiscing elit. Lacus, nisl, lectus nisl sed quis non. Eget porta elit sit tempor eu sit.'
            },
            {
              img: require('../../assets/technologies/back/php.png'),
              head: 'PHP',
              description: 'Lorem ipsum dolor sit amet, consectetur adipiscing elit. Lacus, nisl, lectus nisl sed quis non. Eget porta elit sit tempor eu sit.'
            },
            {
              img: require('../../assets/technologies/back/laravel.png'),
              head: 'Laravel',
              description: 'Lorem ipsum dolor sit amet, consectetur adipiscing elit. Lacus, nisl, lectus nisl sed quis non. Eget porta elit sit tempor eu sit.'
            },
            {
              img: require('../../assets/technologies/back/syphony.png'),
              head: 'Symfony',
              description: 'Lorem ipsum dolor sit amet, consectetur adipiscing elit. Lacus, nisl, lectus nisl sed quis non. Eget porta elit sit tempor eu sit.'
            },
            {
              img: require('../../assets/technologies/back/pytone.png'),
              head: 'Python',
              description: 'Lorem ipsum dolor sit amet, consectetur adipiscing elit. Lacus, nisl, lectus nisl sed quis non. Eget porta elit sit tempor eu sit.'
            },
            {
              img: require('../../assets/technologies/back/django.png'),
              head: 'Django',
              description: 'Lorem ipsum dolor sit amet, consectetur adipiscing elit. Lacus, nisl, lectus nisl sed quis non. Eget porta elit sit tempor eu sit.'
            },
            {
              img: require('../../assets/technologies/back/flack.png'),
              head: 'Flask',
              description: 'Lorem ipsum dolor sit amet, consectetur adipiscing elit. Lacus, nisl, lectus nisl sed quis non. Eget porta elit sit tempor eu sit.'
            },
            {
              img: require('../../assets/technologies/back/golang.png'),
              head: 'Golang',
              description: 'Lorem ipsum dolor sit amet, consectetur adipiscing elit. Lacus, nisl, lectus nisl sed quis non. Eget porta elit sit tempor eu sit.'
            },
            {
              img: require('../../assets/technologies/back/begoo.png'),
              head: 'Begoo',
              description: 'Lorem ipsum dolor sit amet, consectetur adipiscing elit. Lacus, nisl, lectus nisl sed quis non. Eget porta elit sit tempor eu sit.'
            },
            {
              img: require('../../assets/technologies/back/sql.png'),
              head: 'MySQL',
              description: 'Lorem ipsum dolor sit amet, consectetur adipiscing elit. Lacus, nisl, lectus nisl sed quis non. Eget porta elit sit tempor eu sit.'
            },
            {
              img: require('../../assets/technologies/back/postgresql.png'),
              head: 'PostgreSQL',
              description: 'Lorem ipsum dolor sit amet, consectetur adipiscing elit. Lacus, nisl, lectus nisl sed quis non. Eget porta elit sit tempor eu sit.'
            },
            {
              img: require('../../assets/technologies/back/mongodb.png'),
              head: 'MongoDB',
              description: 'Lorem ipsum dolor sit amet, consectetur adipiscing elit. Lacus, nisl, lectus nisl sed quis non. Eget porta elit sit tempor eu sit.'
            }
          ]
        },
        {
          head_1: 'Mobile',
          head_2: 'development',
          description: 'Depending on the requirements, business idea and final expectations, we can choose technologies and implement requests in the most reasonable way.',
          slides: [
            {
              img: require('../../assets/technologies/mobile/objective_C.png'),
              head: 'Objective-C',
              description: 'Lorem ipsum dolor sit amet, consectetur adipiscing elit. Lacus, nisl, lectus nisl sed quis non. Eget porta elit sit tempor eu sit.'
            },
            {
              img: require('../../assets/technologies/mobile/cross_flutter.png'),
              head: 'Flutter',
              description: 'Lorem ipsum dolor sit amet, consectetur adipiscing elit. Lacus, nisl, lectus nisl sed quis non. Eget porta elit sit tempor eu sit.'
            },
            {
              img: require('../../assets/technologies/mobile/java.png'),
              head: 'Java',
              description: 'Lorem ipsum dolor sit amet, consectetur adipiscing elit. Lacus, nisl, lectus nisl sed quis non. Eget porta elit sit tempor eu sit.'
            },
            {
              img: require('../../assets/technologies/mobile/kotlin.png'),
              head: 'Kotlin',
              description: 'Lorem ipsum dolor sit amet, consectetur adipiscing elit. Lacus, nisl, lectus nisl sed quis non. Eget porta elit sit tempor eu sit.'
            },
            {
              img: require('../../assets/technologies/mobile/react.png'),
              head: 'React Native',
              description: 'Lorem ipsum dolor sit amet, consectetur adipiscing elit. Lacus, nisl, lectus nisl sed quis non. Eget porta elit sit tempor eu sit.'
            },
            {
              img: require('../../assets/technologies/mobile/swift.png'),
              head: 'Swift',
              description: 'Lorem ipsum dolor sit amet, consectetur adipiscing elit. Lacus, nisl, lectus nisl sed quis non. Eget porta elit sit tempor eu sit.'
            }
          ]
        }
      ]
    }
  }
}
</script>
<style scoped>
.heading{
  color: #228A43;
  font-size: 50px;
  font-weight: bold;
}
.el-carousel__item h3 {
  color: #475669;
  font-size: 14px;
  opacity: 0.75;
  line-height: 200px;
  margin: 0;
}
.el-carousel--horizontal{
  margin-top: 50px;
  padding-top: 20px;
  width: auto;
  height: 450px;
  overflow-y: hidden;
}
.el-carousel__item:nth-child(2n) {
  margin-top: 15px;
  background-color: black;
  border-radius: 11px;
  display: flex;
  justify-content: center;
  align-items: center;
  flex-direction: column;
}
.el-carousel__item:nth-child(2n+1) {
  margin-top: 15px;
  background-color: black;
  border-radius: 11px;
  display: flex;
  justify-content: center;
  align-items: center;
  flex-direction: column;
}

.el-carousel__item--card.is-active {
  box-shadow: 0 0 44px rgba(255, 255, 255, 0.25);
}
.technologies__content{
  width: 100%;
  height: 100%;
  display: flex;
  justify-content: center;
  align-items: center;
}
.technologies__container{
  width: 1100px;
  padding: 50px 25px;
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
}
.slider__heading{
  text-align: center;
  font-size: 35px;
  color: #FFFFFF;
  font-weight: 700;
  margin: 80px 0 40px 0;
}
.head_1{
  color: #228A43;
}
.technologies__description, .slider__description{
  text-align: center;
  font-size: 23px;
  color: #A5A5A5;
  max-width: 750px;
}
.carousel--img{
  width: 110px;
  height: auto;
}
.carousel--heading{
  font-size: 35px;
  color: #FFFFFF;
  margin: 20px 0;
}
.carousel--description{
  text-align: center;
  font-weight: 300;
  font-size: 17px;
  color: #a5a5a5;
  margin: 0 15px;
}
@media screen and (max-width: 450px){
  .carousel--heading{
    font-size: 18px;
  }
  .carousel--img{
    width: 60%;
    height: auto;
  }
  .carousel--description{
    font-size: 12px;
  }
}
</style>
<style>
.el-carousel__mask{
  background-color: black!important;
}
</style>
