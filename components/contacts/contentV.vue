<template>
  <div class="container">
    <div class="row">
      <div class="col-md-12">
        <div class="spacer"></div>
      </div>
      <div class="col-md-12">
        <h2 class="title-black2">
          Контакты
        </h2>
        <div class="spacer2"></div>
      </div>

      <div class="col-md-6 first_line">
        <h3 class="title">Связаться с нами</h3>

        <div class="contact-text">
          <p class="margin-bottom-25">
            Телефон:
            <span class="devmail">
              <a href="tel://+78612908899" target="_blank"
                >+7 (861) 290-88-99</a
              >
            </span>
          </p>
          <p class="margin-bottom-25">
            Телефон менеджерa доставки:
            <span class="devmail" id="phone_mng">
              <a href="tel://+79385397488" target="_blank"
                >+7 (938) 539-74-88</a
              >
            </span>
          </p>
          <p class="margin-bottom-25">
            E-mail:
            <span class="devmail">
              <a href="mailto:architector.bar@yandex.ru" target="_blank"
                >architector.bar@yandex.ru</a
              >
            </span>
          </p>
        </div>

        <h3 class="title">Время работы</h3>
        <div class="contact-text">
          <p class="margin-bottom-25">с 12:00 до 23:00</p>
        </div>

        <h3 class="title font-size-22">Как нас найти</h3>
        <div style="position:relative;overflow:hidden; border: none;" class="map">
          <a
            href="https://yandex.ru/maps/35/krasnodar/?utm_medium=mapframe&utm_source=maps"
            style="color:#eee;font-size:12px;position:absolute;top:0px;"
            >Краснодар</a
          >
          <a
            href="https://yandex.ru/maps/35/krasnodar/?from=api-maps&ll=38.973997%2C45.033270&mode=usermaps&origin=jsapi_2_1_78&um=constructor%3Ab9f45752b2970c9944e0364b6a51c223ac4a027c7014f1649544403e5cc7f0c5&utm_medium=mapframe&utm_source=maps&z=16"
            style="color:#eee;font-size:12px;position:absolute;top:14px;"
            >Яндекс.Карты — поиск мест и адресов, городской транспорт</a
          >
          <iframe
            src="https://yandex.ru/map-widget/v1/-/CCUMjMxs9A"
            width="100%"
            height="350"
            frameborder="0"
            allowfullscreen="true"
            style="position:relative;"
          ></iframe>
        </div>
      </div>

      <div class="col-md-6 second_line">
        <h3 class="title font-size-22">Реквизиты</h3>
        <div class="contact-text">
          <p class="margin-bottom-25"></p>
          <p class="margin-bottom-25">
            Общество с ограниченной ответственностью «ЛАВР»
            <br />
            ИНН 2311249548
            <br />
            КПП 231001001
            <br />
            ОГРН 1172375100061
            <br />
            Юридический адрес: 350000, г. Краснодар, ул. Красная, д. 118
            <br />
            Почтовый адрес: 350000, г. Краснодар, ул. Красная, д. 118, офис 309
            <br />
            Фактический адрес: 350000, г. Краснодар, ул. Красная, д. 118
            <br />
            ОКВЭД 56.10.1 (Деятельность ресторанов и кафе с полным ресторанным
            обслуживанием, кафетериев, ресторанов быстрого питания и
            самообслуживания)
            <br />
            р/с 40702810026060003655 в ФИЛИАЛ "РОСТОВСКИЙ" АО "АЛЬФА-БАНК"
            <br />
            к/с 30101810500000000207
            <br />
            БИК 046015207
            <br />
            ОКВЭД 56.10
            <br />
            ОКПО 20436596
            <br />
            Директор: Шамян Арсен Рафаэльевич (действует на основании Устава)
          </p>
        </div>
      </div>

      <div class="ligbl">
        <img src="../../assets/ligbl.svg" alt="image" />
      </div>
      <div class="col-md-12 form-wrapper">
        <div
          class="wprt-spacer"
          data-desktop="100"
          data-mobi="100"
          data-smobi="100"
          style="height:100px"
        ></div>
        <h2 class="title-black2 title-menu">Задать вопрос</h2>
        <div class="res_form_container">
          <form id="res_form_black" class="res_form_black">
            <input type="hidden" name="project_name" value="architector-bar" />
            <input
              type="hidden"
              name="admin_email"
              value="sale-architector@yandex.ru"
            />
            <input type="hidden" name="form_sobject" value="Контакты вопрос" />

            <div class="d-flex flex-sm-row flex-column align-items-center">
              <div class="col-md-4">
                <input
                  type="text"
                  placeholder="Вашe имя"
                  id="name"
                  name="Имя"
                  class="input-contact"
                  required=""
                />
              </div>

              <div class="col-md-4">
                <input
                  type="text"
                  placeholder="Ваш телефон"
                  id="telephone"
                  name="Телефон"
                  class="input-contact"
                  required=""
                />
              </div>

              <div class="col-md-4">
                <input
                  type="text"
                  placeholder="Вопрос"
                  id="message"
                  name="Вопрос"
                  class="input-contact"
                  required=""
                />
              </div>
            </div>

            <button class="res_button_black">Отправить</button>
          </form>
        </div>
      </div>
      <div class="col-md-12">
        <div
          class="wprt-spacer"
          data-desktop="120"
          data-mobi="80"
          data-smobi="60"
          style="height:120px"
        ></div>
      </div>
      <div class="watlog">
        <img src="../../assets/watlog.webp" alt="" />
      </div>
    </div>
  </div>
</template>

<script>
export default {};
</script>

<style lang="scss" scoped>

@import 'styles/contacts/contacts.scss'

</style>
