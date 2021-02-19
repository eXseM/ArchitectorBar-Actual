<template>
  <div class="eblan">
    <navbar />
    <modal />
    <Nuxt />
    <to-top />
    <footer-main />
    
    
  </div>
</template>

<script>
import navbar from "~/components/navbar.vue";
import footerMain from '~/components/footer-main.vue';
import ToTop from '~/components/toTop.vue';
import Modal from '~/components/modal.vue';

export default {
  components: {
    navbar,
    footerMain,
    ToTop,
    Modal
  },
};
</script>

<style>
body {
  background-color: #0e0d13;
  font-family: "Montserrat", sans-serif;
  color: #000;
}

* {
  padding: 0;
  margin: 0;
  -webkit-box-sizing: border-box;
  -moz-box-sizing: border-box;
  box-sizing: border-box;
  
}

.eblan{
  position: relative;
}
</style>
