<template>
  <div class="slider">
    <div class="gallery">
      <client-only>
        <flickity class="slider-wrap" ref="flickity" :options="flickityOptions">
          <div class="carousel-cell">
            <div class="slide-text-bg">
              <h3 class="title-white-slider">
                Радужная форель в соусе из копченой вишни
              </h3>
            </div>
            <img src="../../assets/slide1.jpg" alt="" />
          </div>
          <div class="carousel-cell">
            <div class="slide-text-bg">
              <h3 class="title-white-slider">Утка не по пекински</h3>
            </div>
            <img src="../../assets/slide2.jpg" alt="" />
          </div>
          <div class="carousel-cell">
            <div class="slide-text-bg">
              <h3 class="title-white-slider">Калифорния с крабом шиитаки</h3>
            </div>
            <img src="../../assets/slide3.jpg" alt="" />
          </div>
          <div class="carousel-cell">
            <div class="slide-text-bg">
              <h3 class="title-white-slider">
                Хасанские устрицы и Мурманские ежи
              </h3>
            </div>
            <img src="../../assets/slide4.jpg" alt="" />
          </div>
          <div class="carousel-cell">
            <div class="slide-text-bg">
              <h3 class="title-white-slider">Осьминог с пюре из сельдерея</h3>
            </div>
            <img src="../../assets/slide5.jpg" alt="" />
          </div>
        </flickity>
      </client-only>
    </div>
    <div class="container menu_select">
      <div class="row">
        <div class="col-md-12">
          <div class="toggler menu-mob">
            <h3 class="toggle-title">Категории блюд</h3>
            <div class="toggle-content" :class="toggler ? 'toggleEnabled' : 'toggleDisable'">
              <div class="col-md-3 text-center">
                <nuxt-link to="#" class="menu-btn">Закуски</nuxt-link>
                <nuxt-link to="#" class="menu-btn">Димсамы и Гедза</nuxt-link>
                <nuxt-link to="#" class="menu-btn">By Chef Executive</nuxt-link>
              </div>
              <div class="col-md-3 text-center">
                <nuxt-link to="#" class="menu-btn">Салаты</nuxt-link>
                <nuxt-link to="#" class="menu-btn">Морепродукты</nuxt-link>
                <nuxt-link to="#" class="menu-btn">Суши</nuxt-link>
              </div>
              <div class="col-md-3 text-center">
                <nuxt-link to="#" class="menu-btn">WOK Лапша/Рис</nuxt-link>
                <nuxt-link to="#" class="menu-btn">Мясо/птица</nuxt-link>
                <nuxt-link to="#" class="menu-btn">Десерты</nuxt-link>
              </div>
              <div class="col-md-3 text-center">
                <nuxt-link to="#" class="menu-btn">Супы</nuxt-link>
                <nuxt-link to="#" class="menu-btn">Роллы</nuxt-link>
                <nuxt-link to="#" class="menu-btn"
                  >Только в ресторане</nuxt-link
                >
              </div>
            </div>
          </div>
          <div class="menu-desk">
            <div class="col-md-3 text-center">
              <nuxt-link to="#" class="menu-btn">Закуски</nuxt-link>
              <nuxt-link to="#" class="menu-btn">Димсамы и Гедза</nuxt-link>
              <nuxt-link to="#" class="menu-btn">By Chef Executive</nuxt-link>
            </div>
            <div class="col-md-3 text-center">
              <nuxt-link to="#" class="menu-btn">Салаты</nuxt-link>
              <nuxt-link to="#" class="menu-btn">Морепродукты</nuxt-link>
              <nuxt-link to="#" class="menu-btn">Суши</nuxt-link>
            </div>
            <div class="col-md-3 text-center">
              <nuxt-link to="#" class="menu-btn">WOK Лапша/Рис</nuxt-link>
              <nuxt-link to="#" class="menu-btn">Мясо/птица</nuxt-link>
              <nuxt-link to="#" class="menu-btn">Десерты</nuxt-link>
            </div>
            <div class="col-md-3 text-center">
              <nuxt-link to="#" class="menu-btn">Супы</nuxt-link>
              <nuxt-link to="#" class="menu-btn">Роллы</nuxt-link>
              <nuxt-link to="#" class="menu-btn">Только в ресторане</nuxt-link>
            </div>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      flickityOptions: {
        initialIndex: 0,
        prevNextButtons: true,
        pageDots: false,
        wrapAround: true
      }
    };
  }
};
</script>

<style lang="scss">
.slider {
  width: 100%;
  padding: 100px 0;
  background: url(../../assets/bg-menu.webp) center center;
  background-size: cover;
  height: auto;

  .gallery {
    width: 100%;
    margin: auto;
    height: 390px;
    background-color: transparent;

    .slider-wrap {
      width: 100%;
      .carousel-cell {
        .slide-text-bg {
          background-color: rgba(0, 0, 0, 0.73);
          height: 100%;
          top: 0;
          position: absolute;
          width: 50%;
          float: left;
          padding: 50px 15px 50px 25px;
          display: flex;
          align-items: center;
          opacity: 0;

          .title-white-slider {
            font-size: 42px;
            font-weight: 300;
            color: #fff;
            text-align: left;
            line-height: 1.5;
          }
        }

        opacity: 0.1;
        width: 70%;
        height: 390px;
        border-radius: 5px;
        counter-increment: carousel-cell;
        transition: opacity 0.9s;

        img {
          width: 100%;
          margin-top: -100px;
        }
      }
      .is-selected {
        opacity: 1;

        .slide-text-bg {
          opacity: 1;
        }
      }
    }
  }
  .menu_select {
    display: block;

    .row {
      .col-md-12 {
        .menu-mob {
          display: none;
        }
        .menu-desk {
          margin-top: 100px;
          display: flex;
          flex-direction: row;

          .col-md-3 {
            display: flex;
            flex-direction: column;
            justify-content: space-between;
            align-content: space-between;
            align-items: center;
            height: 200px;
            .menu-btn {
              text-align: center;
              background-color: rgba(255, 255, 255, 0.1);
              width: 90%;
              font-family: "Montserrat", sans-serif;
              font-weight: 500;
              display: flex;
              flex-direction: column;
              justify-content: center;
              padding: 7px 20px;
              border: none;
              color: #fff;
              font-size: 14px;
              -webkit-transition: all ease 0.238s;
              -moz-transition: all ease 0.238s;
              transition: all ease 0.238s;
              outline: 0;
              text-decoration: none;
              height: 40px;

              &:hover {
                background-color: rgba(255, 255, 255, 0.3);
                color: #fff;
              }
            }
          }
        }
      }
    }
  }
}

.flickity-button {
  background: transparent;

  &:hover {
    background: transparent;
  }
}
/* big previous & next buttons */
.flickity-prev-next-button {
  width: 70px;
  height: 70px;
}

.flickity-prev-next-button.previous {
  left: 10%;
  background-image: url(../../assets/prev.png);
  background-size: contain;
  background-repeat: no-repeat;
  width: 30px;
  height: 50px;
}
.flickity-prev-next-button.next {
  right: 10%;
  background-image: url(../../assets/next.png);
  background-size: contain;
  background-repeat: no-repeat;
  width: 30px;
  height: 50px;
}
/* icon color */
.flickity-button-icon {
  // fill: rgb(97, 97, 97);
  display: none;
}
/* hide disabled button */
.flickity-button:disabled {
  display: none;
}

@media only screen and (min-width: 1200px) {
  .slider {
    .container {
      max-width: 1200px;
    }
  }
}

@media only screen and (max-width: 991px) {
  .slider {
    padding: 0;

    .gallery {
      height: 290px;
      .slider-wrap {
        height: 290px;
      }
    }
    .menu_select {
      padding: 40px 0;
      width: 100%;
      position: relative;
      background-color: #0e0d13;
      background-image: url(../../assets/bg-menu.webp);
      background-size: cover;

      .row {
        .col-md-12 {
          .menu-desk {
            display: none;
          }
          .menu-mob {
            display: block;

            .toggle-title {
              cursor: pointer;
              font-size: 18px;
              font-weight: 400;
              text-transform: uppercase;
              padding: 15px 40px 15px 40px;
              color: #eeeeed;
              border: 1px solid #eeeeed;
              margin: 50px 30px;
              border-radius: 3px;
              position: relative;
              text-align: center;
              -webkit-transition: all ease 0.238s;
              -moz-transition: all ease 0.238s;
              transition: all ease 0.238s;

              &::before {
                content: "\f107";
                font-family: "FontAwesome";
                font-weight: normal;
                line-height: normal;
                position: absolute;
                left: auto;
                right: 20px;
                top: 50%;
                -webkit-transform: translate3d(0, -50%, 0);
                -moz-transform: translate3d(0, -50%, 0);
                transform: translate3d(0, -50%, 0);
              }
            }

            .toggle-content {
              width: 100%;
              padding: 20px 20px 35px;
              display: none;
              flex-direction: column;
              justify-content: center;
              align-items: center;
              align-content: center;

              .col-md-3 {
                display: flex;
                flex-direction: column;
                justify-content: space-between;
                align-items: center;
                height: 200px;
                margin-bottom: 40px;

                .menu-btn {
                  text-align: center;
                  background-color: rgba(255, 255, 255, 0.1);
                  width: 90%;
                  font-family: "Montserrat", sans-serif;
                  font-weight: 500;
                  display: flex;
                  flex-direction: column;
                  justify-content: center;
                  border: none;
                  color: #fff;
                  font-size: 14px;
                  -webkit-transition: all ease 0.238s;
                  -moz-transition: all ease 0.238s;
                  transition: all ease 0.238s;
                  height: 40px;
                }
              }
            }
          }
        }
      }
    }
  }
}

@media only screen and (max-width: 640px) {
  .slider {
    .gallery {
      .slider-wrap {
        .carousel-cell {
          height: 215px;
          width: 100%;

          img {
            width: 100%;
            margin-top: 0;
          }
          .slide-text-bg {
            width: 100%;

            .title-white-slider {
              text-align: center;
              margin-top: 25px;
              padding: 0 60px;
            }
          }
        }
      }
    }
  }
}

@media only screen and (max-width: 540px) {
  .slider {
    .gallery {
      height: 215px;
    }
  }

  .flickity-prev-next-button.previous {
    left: 5%;
    top: 35%;
    width: 30px;
    height: 50px;
  }
  .flickity-prev-next-button.next {
    right: 5%;
    width: 30px;
    height: 50px;
    top: 35%;
  }
}

@media only screen and (max-width: 480px) {
  .slider {
    height: auto;
    .gallery {
      .slider-wrap {
        .slide-text-bg {
          .title-white-slider {
            margin-top: 30px;
            font-size: 18px !important;
          }
        }
      }
    }
  }
}
</style>
