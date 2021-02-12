<template>
  <div class="footer">
    <div class="container">
      <div class="footer__content">
        <div class="copy">© 2021 - All Right Reserved</div>
        <div class="authors">
          <a
            href="https://instagram.com/cudo_design?igshid=1eaggttkg6mro"
            target="_blank"
            >DESIGN BY CUDO</a
          >
        </div>
      </div>
      <div class="footer__menu">
        <p>Краснодар ул. Красная, 118</p>
        <div class="icons">
          <img src="../assets/call.svg" alt="" />
          <img src="../assets/insta.svg" alt="" />
          <img src="../assets/social.svg" alt="" />
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {};
</script>

<style lang="scss" scoped>
@media only screen and (min-width: 1200px) {
  .footer {
    .container {
      width: 1200px;
    }
  }
}

@media only screen and (max-width: 1200px) {
  .footer {
    &__menu {
      width: 50%;
    }
  }
}

.footer {
  position: relative;
  background-color: rgba(16, 16, 16, 0.6);
  width: 100%;
  height: 66px;

  .container {
    width: 1170px;
    max-width: 100%;
    height: 100%;
    display: flex;
    flex-direction: row;
    justify-content: center;
  }

  &__content {
    width: 43%;
    display: flex;
    flex-direction: row;
    justify-content: space-between;
    align-items: center;
    align-content: center;

    .copy {
      font-size: 12px;
      color: #fff;
      margin-left: -60px;
    }

    .authors {
      a {
        color: #fff;
        text-decoration: none;
        font-size: 12px;
      }
    }
  }

  &__menu {
    width: 35%;
    display: flex;
    flex-direction: row;
    justify-content: flex-end;
    align-items: center;

    p {
      padding-top: 17px;
      color: #fff;
      font-size: 12px;
    }

    .icons {
      margin-right: -60px;
      width: 40%;
      height: 30%;
      img {
        padding-left: 30px;
        height: 100%;
      }
    }
  }
}
</style>
