<template>
  <div>
    <navbar />
    <Nuxt />
    <to-top />
    <footer-main />
  </div>
</template>

<script>
import navbar from "~/components/navbar.vue";
import footerMain from '~/components/footer-main.vue';
import ToTop from '~/components/toTop.vue';

export default {
  components: {
    navbar,
    footerMain,
    ToTop
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
</style>
