<template>
  <div class="reservation wprt-section2" id="reserved">
    <div class="blgl">
      <div class="container">
        <div class="row">
          <div class="col-md-12">
            <div class="wprt-spacer"></div>
            <h3 class="title-white mb-20">Бронирование</h3>
            <div class="res_form_container">
              <form class="res_form">
                <input type="hidden" name="" />
                <input type="hidden" name="" />
                <input type="hidden" name="" />
                <div class="form_inner">
                  <div class="col-md-4">
                    <p class="dtp">Имя и фамилия</p>
                    <input
                      type="text"
                      placeholder="Ваше имя"
                      name="name"
                      id="name"
                      class="res_input"
                      required
                    />
                  </div>
                  <div class="col-md-4">
                    <p class="dtp">Почта</p>
                    <input
                      type="text"
                      placeholder="Ваш E-mail"
                      id="email"
                      name="e-mail"
                      class="res_input"
                      required
                    />
                  </div>
                  <div class="col-md-4">
                    <p class="dtp">Телефон</p>
                    <client-only> 
                    <masked-input
                      mask="\+\7 (111) 111-11-11"
                      placeholder="Ваш телефон"
                      @input="rawVal = arguments[1]"
                      class="res_input"
                      required
                    />
                    </client-only>
                  </div>
                  <div class="col-md-4">
                    <p class="dtp">Дата</p>
                    <client-only>
                      <datepicker
                        v-model="date"
                        class="res_input datePicker"
                        placeholder="Укажите дату"
                        :language="ru"
                        required
                        @input="onDate"
                      ></datepicker>
                    </client-only>
                  </div>
                  <div class="col-md-4">
                    <p class="dtp">Время</p>
                    <select name="time" class="res_select">
                      <option selected disabled>Укажите время</option>
                      <option
                        v-for="item in times"
                        :item="item"
                        :key="item.key"
                        >{{ item.time }}</option
                      >
                    </select>
                  </div>
                  <div class="col-md-4 last">
                    <p class="dtp">Количество персон</p>
                    <input
                      type="number"
                      name="persones"
                      placeholder="Укажите число"
                      required
                      class="res_input"
                    />
                  </div>
                </div>
                <button class="res_btn">Забронировать</button>
              </form>
            </div>
            <div class="rhombus2">
              <img src="../../assets/rhombus2.svg" alt="" />
            </div>
          </div>
          <div class="col-md-12"><div class="wprt-spacer"></div></div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import { ru } from "vuejs-datepicker/dist/locale";

export default {
  components: {},
  data() {
    return {
      times: [
        { time: "12:00" },
        { time: "13:00" },
        { time: "14:00" },
        { time: "15:00" },
        { time: "16:00" },
        { time: "17:00" },
        { time: "18:00" },
        { time: "19:00" },
        { time: "20:00" },
        { time: "21:00" },
        { time: "22:00" },
        { time: "23:00" }
      ],
      date: null,
      ru: ru,
    };
  },
  methods:{
    onDate(){
      let reservDate = new Date(this.date).toLocaleDateString();
    }
  },
};
</script>

<style lang="scss">
@import "styles/main/reserv.scss";
</style>
