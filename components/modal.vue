<template>
  <div class="modal" v-if="isActive" @click="close()">
    <!-- <div :class="showModal ? 'isActive' : 'inActive'"> -->
    <div class="modal-window">
      <ShareNetwork
        network="telegram"
        url="https://architector.bar/"
        title="Архитектор бар"
      ></ShareNetwork>
    </div>
  </div>
</template>
<script>
export default {
  data() {
    return {
      isActive: false,
    };
  },
  methods: {
    close() {
      this.isActive = false;
    },
  },
  created() {
    this.$bus.$on("open-share-modal", () => (this.isActive = true));
    this.$bus.$on("close-share-modal", () => (this.isActive = false));
  },
  beforeDestroy() {
    this.$bus.$off("open-share-modal");
    this.$bus.$off("close-share-modal");
  }
};
</script>

<style lang="scss" scoped>
.modal {
  width: 100%;
  height: 100%;
  position: absolute;
  left: 0;
  top: 0;
  background: crimson;
  z-index: 5555;
  display: block;
  .modal-window {
    z-index: 5556;
    width: 300px;
    height: 300px;
    background: #323232;
    // Ladno so stilyami pobus
  }
}
</style>
