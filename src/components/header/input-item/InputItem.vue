<template>
  <div class="wrapper">
    <input type="text" placeholder="search..." />
    <i class="iconfont icon-search"></i>
  </div>
</template>
<script>
export default {
  name: "input-item",
};
</script>
<style lang="scss" scoped>
.wrapper {
  background-color: #f7f7f7;
  padding: 0 10px;
  border-radius: 18px;
  & input {
    border: none;
    outline: none;
    padding: 0 10px;
    height: 40px;
    font-size: 16px;
    background-color: #f7f7f7;
  }
  & input::-webkit-input-placeholder {
    color: #c5c3c3;
  }
  & input:-moz-placeholder {
    color: #c5c3c3;
  }
  & input:-ms-input-placeholder {
    color: #c5c3c3;
  }
  & .icon-search {
    color: #b4b4b4;
    font-size: 20px;
    font-weight: bold;
    cursor: pointer;
  }
}
</style>
