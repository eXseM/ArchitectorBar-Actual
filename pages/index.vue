<template>
  <div>
    <main-title />
    <main-about />
    <reserv />
  </div>
</template>

<script>

import MainTitle from '~/components/main/mainTitle.vue'
import MainAbout from '~/components/main/mainAbout.vue'
import reserv from '~/components/main/reserv.vue'


export default {
  components:{
    MainTitle,
    MainAbout,
    reserv
  }
}
</script>
<style>

</style>
