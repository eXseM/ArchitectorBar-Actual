<template>
  <header class="nav">
    <div class="nav__wrapper container">
      <div class="logo">
        <nuxt-link to="/"
          ><img src="../assets/logo.png" alt="" width="38"
        />
        </nuxt-link>
      </div>
      <div class="menu-main">
        <div class="menu-main__item">
          <nuxt-link to="/">Главная</nuxt-link>
        </div>
        <div class="menu-main__item">
          <nuxt-link to="/menu">Меню</nuxt-link>
        </div>
        <div class="menu-main__item">
          <nuxt-link to="/delivery">Доставка</nuxt-link>
        </div>
        <div class="menu-main__item">
          <nuxt-link to="/contacts">Контакты</nuxt-link>
        </div>
      </div>
      <div class="menu-mob">
        <label class="btn-menu" @click="showMenu = !showMenu">
          <span class="first" v-if="!showMenu"></span>
        </label>
        <ul :class="showMenu ? 'activeMenu' : 'hideMenu'">
          <li @click="showMenu = !showMenu"><nuxt-link to="/" >Главная</nuxt-link></li>
          <li @click="showMenu = !showMenu"><nuxt-link to="/menu">Меню</nuxt-link></li>
          <li @click="showMenu = !showMenu"><nuxt-link to="/delivery">Доставка</nuxt-link></li>
          <li @click="showMenu = !showMenu"><nuxt-link to="/contacts">Контакты</nuxt-link></li>
          <div class="pd-menu">
            <nuxt-link to="#reserved">Забронировать стол</nuxt-link>
            <div class="soc-add">
              <a href="tel: +79385397488"><img src="../assets/call.svg" alt="" width="20" /></a>
              <a href="https://www.instagram.com/architector.cafe_bar/?igshid=1iozjn6pu1xaf" target="_blank"><img src="../assets/insta.svg" alt="" width="20" /></a>
              <img src="../assets/social.svg" alt="" width="20" @click="showModal"/>
            </div>
            <p>Краснодар ул. Красная, 118</p>
          </div>
          <label class="btn-menu" @click="showMenu = !showMenu">
            <span class="first2"></span>
          </label>
        </ul>
        
      </div>
      <div class="social">
        <div class="inst"><a href="https://www.instagram.com/architector.cafe_bar/?igshid=1iozjn6pu1xaf" target="_blank"><img src="../assets/insta.svg" alt="" /></a></div>
        <div class="phone"><a href="tel: +79385397488"><img src="../assets/call.svg" alt="" /> </a></div>
        <div class="share"><img src="../assets/social.svg" alt="" @click="showModal" /></div>
      </div>
    </div>
  </header>
</template>

<script>
export default {
  data() {
    return {
      show: false,
      showMenu: false,
    };
  },
  methods: {
    showModal () {
      this.$bus.$emit('open-share-modal')
    }
  }
};
</script>

<style lang="scss" scoped>
@import "styles/navigation.scss";
</style>
