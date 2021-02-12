<template>
  <header class="nav">
    <div class="nav__wrapper container">
      <div class="logo">
        <nuxt-link to="/"><img src="../assets/logo.png" alt="" width="38" /></nuxt-link>
      </div>
      <div class="menu-main">
        <div class="menu-main__item">
          <nuxt-link to="/" style="color: #fff">Главная</nuxt-link>
        </div>
        <div class="menu-main__item"><nuxt-link to="/menu">Меню</nuxt-link></div>
        <div class="menu-main__item"><nuxt-link to="/delivery">Доставка</nuxt-link></div>
        <div class="menu-main__item"><nuxt-link to="/contacts">Контакты</nuxt-link></div>
      </div>
      <div class="menu-mob"></div>
      <div class="social">
        <div class="inst"><img src="../assets/insta.svg" alt="" /></div>
        <div class="phone"><img src="../assets/call.svg" alt="" /></div>
        <div class="share"><img src="../assets/social.svg" alt="" /></div>
      </div>
    </div>
  </header>
</template>

<script>
export default {};
</script>

<style lang="scss" scoped>
.nav {
  position: sticky;
  top:0;
  background: rgba(13, 15, 19, 0.95);
  width: 100%;
  display: flex;
  justify-content: center;
  font-family: montserrat, serif;
  z-index: 99999;

  &__wrapper {

    position: relative;
    padding-top: 15px;
    padding-bottom: 15px;
    display: flex;

    .menu-main {
      display: flex;
      //background: #ffffff;
      width: 30%;
      justify-content: space-between;
      align-content: center;
      align-items: center;
      margin-left: 35px;

      &__item {
        padding-right: 35px;
        a {
          text-decoration: none;
          font-size: 14px;
          font-weight: 500;
          color: rgba(255, 255, 255, 0.3);
          text-transform: uppercase;
        }
      }
    }
    .social {
      position: absolute;
      right: 0;
      top: 0;
      width: 20%;
      height: 100%;
      display: flex;
      flex-direction: row;
      align-content: center;
      justify-content: flex-end;
      align-items: center;

      div {
        padding-left: 25px;

        img {
          width: 25px;
          height: 25px;
        }
      }
    }
  }
}

@media only screen and (min-width: 1200px){
  .nav{
    .container{
      max-width: 1200px;
    }
  }
}
@media (min-width: 992px){
  .nav{
    .container{
      width: 970px;
    }

  }
}

@media only screen and (max-width: 1440px){
  .nav{
    &__wrapper{
      width: 100%;
    }
  }
}


@media only screen and (max-width: 1200px){
  .nav{
    &__wrapper{
      width: 100%;
      display: flex;
      flex-direction: row;
    }
  }
}
</style>
