<template>
  <div class="btnTop">
    <div :class="showArrow ? 'showBtn' : 'hideBtn'" @click="ToTop"></div>
  </div>
</template>

<script>
export default {
  data(){
    return {
      showArrow: false,
    }
  },
  methods:{
    ToTop(){
      window.scrollTo(0, 0)
    }
  },
  mounted() {
    window.addEventListener("scroll", () => {
      if (window.pageYOffset > 1000) {
        this.showArrow = true;
      } else {
        this.showArrow = false;
      }
    });
  }
};
</script>

<style lang="scss" scoped>

.hideBtn {
  display: none;
}
.showBtn {
  display: block;
  text-align: center;
  line-height: 30px;
  color: #444;
  cursor: pointer;
  position: fixed;
  bottom: 15px;
  right: 15px;
  z-index: 99999;
  width: 40px;
  height: 40px;
  background-color: #eeeeed;
  border: 1px solid #0d0f13;
  border-radius: 3px;

    &::before {
      content: "";
      position: absolute;
      width: 10px;
      height: 10px;
      border-left: 1px solid #0d0f13;
      border-top: 1px solid #0d0f13;
      top: 6px;
      bottom: 0;
      left: 0;
      right: 0;
      margin: auto;
      transform: rotate(45deg);
  }
}
</style>
