<template>
  <div class="modal" v-if="isActive" @click="test($event)">
    <div class="block">
      <p class="block-text"> Поделиться! </p>
      <div class="social-share-btn">
        <ShareNetwork
          network="VK"
          url="https://architector.bar/"
          title="Архитектор бар"
        >
          <img src="../assets/vk.png" alt="" width="24" height="24" />
        </ShareNetwork>
        <ShareNetwork
          network="facebook"
          url="https://architector.bar/"
          title="Архитектор бар"
        >
          <img src="../assets/facebook.png" alt="" width="24" height="24" />
        </ShareNetwork>
        <ShareNetwork
          network="WhatsApp"
          url="https://architector.bar/"
          title="Архитектор бар"
        >
          <img src="../assets/whatsapp.png" alt="" width="24" height="24" />
        </ShareNetwork>
        <ShareNetwork
          network="Telegram"
          url="https://architector.bar/"
          title="Архитектор бар"
        >
          <img src="../assets/telegram.png" alt="" width="24" height="24" />
        </ShareNetwork>
      </div>
    </div>
  </div>
</template>
<script>
export default {
  data() {
    return {
      isActive: false
    };
  },
  methods: {
    close() {
      this.isActive = false;
    },
    test(event) {
      console.log(event);
      if (!event.target.className.includes("block")) {
        return this.close();
      }
    }
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
  position: fixed;
  left: 0;
  top: 0;
  background: rgba(0, 0, 0, 0.7);
  display: flex;
  transition: 0.3s ease-in-out;
  flex-direction: column;
  justify-content: center;
  align-items: center;
  .block {
    width: 218px;
    height: 123px;
    background: #fff;
    margin: auto;
    margin-top: 350px;
    display: flex;
    flex-direction: column;
    justify-content: space-evenly;
    align-items: center;

    .block-text{
      font-size: 18px;
    }

    .social-share-btn {
      width: 50%;
    }
  }
}
</style>
