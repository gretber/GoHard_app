<template>
  <footer>
    <section class="footer__container">
      <a href="https://www.upwork.com/o/companies/~0183f849d3eab1108c/" target="_blank" class="item upwork__link">
        <img src="@/assets/footer/link.svg" alt="linkedin_link">
        <div class="description">
          UpWork
          LinkId
        </div>
      </a>
      <div class="item">
        <img src="@/assets/footer/mail.svg" alt="linkedin_link">
        <div class="description">
          <a class="description" href="mailto:busdev@gohard.tech">busdev@gohard.tech</a>
          <a class="description" href="mailto:hr@gohard.tech">hr@gohard.tech</a>
        </div>
      </div>
      <a href="tel:+38 (012) 1234567" target="_blank" class="item">
        <img src="@/assets/footer/link.svg" alt="linkedin_link">
        <div class="description">
          +38 (012) 1234567
        </div>
      </a>
    </section>
  </footer>
</template>
<style scoped>
  footer{
    font-family: 'Nunito', sans-serif;
    width: 100%;
    height: 98px;
    background-color: black;
    box-shadow: 0px -1px 5px rgba(255, 255, 255, 0.25);
    display: flex;
    justify-content: center;
  }
  .footer__container{
    width: 1100px;
    height: 100%;
    display: flex;
    justify-content: space-around;
    align-items: flex-start;
    margin-top: 15px;
  }
  .item{
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
  }
  .upwork__link{
    max-width: 90px;
  }
  .item:link{
    text-decoration: none;
  }
  .description:link{
    text-decoration: none;
  }
  img{
    margin-bottom: 10px;
  }
  .description{
    font-weight: 700;
    font-size: 15px;
    text-align: center;
    color: #fff;
    display: flex;
    flex-direction: column;
  }
  @media screen and (max-width: 550px){
    footer{
      height: 75px;
      padding-bottom: 15px;
    }
    img{
      width: 25px;
      height: 25px;
    }
    .description{
      font-size: 10px;
    }
  }
</style>
