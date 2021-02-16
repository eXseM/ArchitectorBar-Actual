<template>
  <div class="delivery">
    <div class="container">
      <div class="row">
        <div class="col-md-12">
          <div class="spacer1"></div>
        </div>
        <div class="col-md-12">
          <h2 class="title-black">Условия доставки</h2>
          <div class="spacer2"></div>
        </div>
        <div class="rowall">
          <div class="col-md-6 col1">
            <div class="about-del">
              <div class="mb-25 con-1">
                Время приёма заказов на доставку ежедневно с 12:00 до 23:00.
              </div>
              <div class="mb-25 con-2">
                Так же можно сделать предварительный заказ или заказ к
                определенному времени, при этом доставка ко времени
                осуществляется с временным интервалом плюс/минус 10 минут от
                указанного Вами времени.
              </div>
              <div class="mb-25 con-3">
                Стоимость доставки рассчитывается автоматически в зависимости от
                зоны при оформлении заказа и указании точного адреса доставки.
              </div>
              <div class="mb-25 con-4">
                Мы заботимся о качестве наших блюд и о вашем времени ожидания.
                Все возникшие вопросы или претензии вы можете решить, связавшись
                с менеджером доставки по телефону
                <span class="devmail"><a href="tel:">+7 938 539-74-88</a></span
                >. В случае отсутствия возможности оперативно передать нам
                информацию о некачественном продукте, вам необходимо сохранить
                чек и блюда, вызвавшие подозрения. Претензию необходимо
                направить на адрес
                <span class="devmail"
                  ><a href="mailto:">architector.bar@yandex.ru</a></span
                >
                Вам ответят в течение суток.
              </div>
              <div class="mb-25 con-5">
                Время доставки определяется менеджером и сообщается по телефону
                при подтверждении заказа. Среднее время доставки 60 минут. В
                будние дни с 17:00 до 20.00 время доставки увеличивается. В
                случае форс-мажорных обстоятельств или при большом количестве
                заказов время доставки может быть увеличено. При возникновении
                технических причин (перекрытие дорог, отключение электроэнергии,
                водоснабжения и т.п.) заказы временно могут не приниматься.
              </div>
              <div class="mb-25 con-6">
                Если по каким-то причинам Ваш заказ не был доставлен в первый
                раз (не работал домофон либо Вас не оказалось на месте и т.п),
                то стоимость повторной доставки будет формироваться
                индивидуально.
              </div>
              <div class="mb-25 con-7">
                Заказ может оформить лицо, достигшее 14 лет (в соответствии со
                статьей 26 ГК РФ - Дееспособность несовершеннолетних в возрасте
                от четырнадцати до восемнадцати лет).
              </div>
              <div class="mb-25 con-8">
                Доставка маленьких суши, и прочих мелкоразмерных блюд, может
                осуществляться по несколько порций в одном ланч-боксе.
              </div>
            </div>
          </div>
          <div class="col-md-6 col2">
            <div class="about-del">
              <img src="../../assets/dostavka2.png" alt="" />
            </div>
          </div>
        </div>
        <div class="ligbl">
          <img src="../../assets/ligbl.svg" alt="" />
        </div>
        <div class="col-md-12"><div class="spacer3"></div></div>
        <div class="col-md-12"><div class="spacer4"></div></div>
        <div class="watlog"><img src="../../assets/watlog.png" alt=""></div>
      </div>
    </div>
  </div>
</template>

<script>
export default {};
</script>

<style lang="scss" scoped>
.delivery {
  background-color: #eeeeed;
  font-family: "Montserrat", sans-serif;
  position: relative;

  .container {
    .row {
      .col-md-12 {
        .spacer1 {
          height: 100px;
        }

        .spacer2 {
          height: 60px;
        }

        .title-black {
          line-height: normal;
          margin-bottom: 10px;
          display: block;
          font-size: 50px;
          color: #0d0f13;
          font-weight: 400;
          padding-left: 0;
          margin-left: -5px;
        }
      }
      .rowall {
        display: flex;
        flex-flow: wrap;
        width: 100%;
        padding-bottom: 250px;

        .col1 {
          order: 0;

          .about-del {
            padding-left: 0;
            width: 100%;
            text-align: left;

            div.mb-25 {
              margin-bottom: 25px;
              font-size: 18px;
              line-height: 1.875;

              .devmail {
                a {
                  color: #161616;
                  font-weight: 600;
                  text-decoration: underline;
                }
              }
            }
            .con-1 {
              &:before {
                content: "1";
                color: #fff;
                background-color: #0d0f13;
                border: none;
                border-radius: 2px;
                height: 32px;
                width: 32px;
                font-size: 16px;
                display: inline-block;
                text-align: center;
                margin-right: 15px;
                line-height: 1.9;
              }
            }
            .con-2 {
              &:before {
                content: "2";
                color: #fff;
                background-color: #0d0f13;
                border: none;
                border-radius: 2px;
                height: 32px;
                width: 32px;
                font-size: 16px;
                display: inline-block;
                text-align: center;
                margin-right: 15px;
                line-height: 1.9;
              }
            }
            .con-3 {
              &:before {
                content: "3";
                color: #fff;
                background-color: #0d0f13;
                border: none;
                border-radius: 2px;
                height: 32px;
                width: 32px;
                font-size: 16px;
                display: inline-block;
                text-align: center;
                margin-right: 15px;
                line-height: 1.9;
              }
            }
            .con-4 {
              &:before {
                content: "4";
                color: #fff;
                background-color: #0d0f13;
                border: none;
                border-radius: 2px;
                height: 32px;
                width: 32px;
                font-size: 16px;
                display: inline-block;
                text-align: center;
                margin-right: 15px;
                line-height: 1.9;
              }
            }
            .con-5 {
              &:before {
                content: "5";
                color: #fff;
                background-color: #0d0f13;
                border: none;
                border-radius: 2px;
                height: 32px;
                width: 32px;
                font-size: 16px;
                display: inline-block;
                text-align: center;
                margin-right: 15px;
                line-height: 1.9;
              }
            }
            .con-6 {
              &:before {
                content: "6";
                color: #fff;
                background-color: #0d0f13;
                border: none;
                border-radius: 2px;
                height: 32px;
                width: 32px;
                font-size: 16px;
                display: inline-block;
                text-align: center;
                margin-right: 15px;
                line-height: 1.9;
              }
            }
            .con-7 {
              &:before {
                content: "7";
                color: #fff;
                background-color: #0d0f13;
                border: none;
                border-radius: 2px;
                height: 32px;
                width: 32px;
                font-size: 16px;
                display: inline-block;
                text-align: center;
                margin-right: 15px;
                line-height: 1.9;
              }
            }
            .con-8 {
              &:before {
                content: "8";
                color: #fff;
                background-color: #0d0f13;
                border: none;
                border-radius: 2px;
                height: 32px;
                width: 32px;
                font-size: 16px;
                display: inline-block;
                text-align: center;
                margin-right: 15px;
                line-height: 1.9;
              }
            }
          }
        }
        .col2{
            .about-del{
                padding-left: 0;
                width: 100%;
                text-align: left;
                img{
                    max-width: 100%;
                    height: auto;
                }
            }
        }
      }
      .ligbl{
          display: block;
          position: absolute;
          right: 7.5%;
          top: 155px;
          width: 95px;

          img{
              max-width: 100%;
              height: auto;
          }
      }
      .watlog{
          position: absolute;
          left: -190px;
          bottom: 0;
          width: 400px;
          height: auto;

          img{
              height: auto;
              max-width: 100%;
          }
      }
    }
  }
}

@media only screen and (min-width: 1200px) {
  .container {
    max-width: 1200px;
  }
}
@media only screen and (max-width: 991px){
  .delivery{
    .container{
      .row{
        .col-md-12{
          .title-black{
            font-size: 32px;
            padding-left: 4%;
          }
          .spacer2{
            display: none;
          }
        }
        .rowall{
          flex-direction: column;
          padding-bottom: 180px;
          .col1{
            order: 1;
            max-width: 100%;
            .about-del{
              padding-left: 4%;
            }
          }
          .col2{
            order: 0;
            max-width: 100%;
          }
        }
        .ligbl{
          display: none;
        }
        .watlog{
          width: 250px;
          left: -120px;
          bottom: 25px;
        }
      }
    }
  }
}

</style>
