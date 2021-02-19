<template>
  <div class="title">
    <div class="container">
      <div class="title__wrapper">
        <div class="title__inner">
          <div class="bg-mob"><img src="../../assets/wok-mob.webp" alt="" /></div>
          <div class="col-md-6">
            <div class="log-wrapper">
              <div class="log-inner image-wrap">
                <img src="../../assets/ar-logo.png" alt="" />
              </div>
            </div>
            <h1 class="title-heading">Конструктивизм паназиатской кухни</h1>
            <div class="text-main">
              <p class="text-desk">
                Кафе-бар паназиатской кухни с авторскими коктейлями и
                атмосферными вечеринками, расположенный в самом сердце города.
                Меню «Архитектора» создавалось лучшими шеф-поварами страны,
                основываясь на современных мировых кулинарных тенденциях.
              </p>
              <p class="text-mob">
                Кафе-бар паназиатской кухни с авторскими коктейлями и
                атмосферными вечеринками, расположенный в самом сердце города.
              </p>
              <div class="buttons">
                <nuxt-link to="#reserved" class="btn reserv-btn outline"
                  >Забронировать стол</nuxt-link
                >
                <nuxt-link to="/menu" class="btn outline">Оформить доставку</nuxt-link>
              </div>
            </div>
          </div>
          <div class="bg-desk"><img src="../../assets/wok-desk.webp" alt="" /></div>
          <div class="bg-tab"><img src="../../assets/wok-tab.webp" alt="" /></div>
          <div class="rhombus"><img src="../../assets/rhombus.svg" alt="" /></div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {};
</script>

<style lang="scss" scoped>

@import 'styles/main/title.scss';


</style>
