<template>
  <div class="wrapper">
    <div class="logo">
      <img src="https://cn.vuejs.org/images/logo.png" alt="logo">
    </div>
    <div class="header-item">
      <span>Dashboard</span>
      <span>Services</span>
      <span>History</span>
      <span>Actions</span>
    </div>
    <input-item class="input-item"/>
  </div>
</template>
<script>
import InputItem from "./input-item/InputItem.vue";
export default {
  name: "HeaderMenu",
  components: {
    InputItem
  }
};
</script>
<style lang="scss" scoped>
.wrapper {
  display: flex;
  flex-direction: row;
  justify-content: space-between;
  align-items: center;
  .logo {
    width: 50px;
    height: 50px;
    img {
      width: 100%;
      height: 100%;
    }
  }
  .header-item {
    height: 40px;
    width: calc(100% - 50px - 400px - 50px);
    margin-left: 50px;
    display: flex;
    flex-direction: row;
    justify-content: space-around;
    & span {
      line-height: 40px;
      color: #777;
      font-size: 18px;
      cursor: pointer;
    }
    & span:first-child {
      color: #000;
      font-weight: bold;
    }
    & span:hover {
      color: #333;
    }
  }
}
</style>

