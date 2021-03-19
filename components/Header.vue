<template>
  <header>
    <div class="header__container">
      <nuxt-link class="logo" to="/">
        <img class="logo" src="@/assets/header/logo.png" alt="logo">
      </nuxt-link>
      <nav class="main__manu">
        <nuxt-link
          v-for="(link, index) of links"
          :key="index"
          class="nav-link"
          :to="link.to"
        >
          {{ link.name }}
        </nuxt-link>
      </nav>
      <div class="hamburger-menu">
        <input id="menu__toggle" type="checkbox">
        <label class="menu__btn" for="menu__toggle" @click="menu = !menu">
          <span class="first" />
          <span class="second" />
          <span class="third" />
        </label>
        <ul v-if="menu" class="menu__box">
          <li v-for="(link, index) of links" :key="index" @click="menu = !menu">
            <nuxt-link tag="ul" class="menu__item" :to="link.to">
              {{ link.name }}
            </nuxt-link>
          </li>
        </ul>
      </div>
    </div>
  </header>
</template>
<script>
export default {
  data () {
    return {
      menu: false,
      links: [
        { name: 'Company', to: '/' },
        { name: 'About us', to: '/about-us' },
        { name: 'Our Services', to: '/our-services' },
        { name: 'Technologies', to: '/technologies' },
        { name: 'Portfolio', to: '/portfolio' }
      ]
    }
  }
}
</script>
<style scoped>
  header{
    width: 100%;
    height: 100px;
    background-color: rgba(0, 0, 0, 0.8);
    position: fixed;
    top: 0;
    display: flex;
    justify-content: center;
    z-index: 10;
    box-shadow: 0px 4px 6px rgba(180, 180, 180, 0.1);
  }
  a.nuxt-link-exact-active {
    color: #228A43;
  }
  a.nuxt-link-exact-active::before {
    width: 100%;
  }
  .header__container{
    margin: 0px 25px;
    width: 1100px;
    height: 100%;
    display: flex;
    justify-content: space-between;
    align-items: center;
  }
  .logo{
    z-index: 1000;
    width: 163px;
    height: 116px;
  }
  .nav-link{
    color: #fff;
    text-decoration: none;
    font-weight: bold;
    font-size: 15px;
    line-height: 20px;
    font-family: 'Nunito', sans-serif;
    margin-left: 24px;
    transition: all 0.3s;
    position: relative;
  }
  .nav-link::before{
    position: absolute;
    left: -1px;
    bottom: -5px;
    content: "";
    width: 0px;
    height: 2px;
    border-radius: 20%;
    background-color: #228A43;
    transition: all 0.3s;
  }
  .nav-link:hover{
    color: #228A43;
  }
  .nav-link:hover.nav-link::before{
    width: 100%;
  }
  #menu__toggle {
    opacity: 0;
  }
  .hamburger-menu{
    display: none;
  }
  .menu__btn {
    flex-direction: column;
    align-items: flex-end;
    justify-content: space-between;
    position: fixed;
    top: 30px;
    right: 30px;
    width: 50px;
    height: 30px;
    cursor: pointer;
    z-index: 1;
    transition: all 0.3s;
  }

  .menu__btn span {
    height: 4px;
    background-color: #fff;
    border-radius: 15px;
  }
  .first{
    width: 100%;
  }
  .second {
    width: 60%;
  }
  .third{
    width: 30%;
  }
  .menu__box {
    display: block;
    position: fixed;
    top: 0;
    left: 0;
    width: 100%;
    height: 250px;
    margin: 0;
    padding: 80px 0;
    list-style: none;
    text-align: center;
    background-color: black;
  }
  /* элементы меню */
  .menu__item {
    display: block;
    padding: 12px 24px;
    color: #fff;
    font-size: 30px;
    font-weight: 600;
    text-decoration: none;
    border-bottom: 0.5px solid #525252;
    cursor: pointer;
  }
  .nuxt-link-exact-active{
    color: #228A43;
  }
  .menu__item:hover {
    color: #228A43;
  }
  .main__manu{
    width: 100%;
    display: flex;
    justify-content: flex-end;
    align-items: center;
  }

  @media screen and (max-width: 740px) {
    .hamburger-menu{
      display: block;
    }
    .menu__btn{
      display: flex;
    }
    .main__manu{
      display: none;
    }
  }
</style>
