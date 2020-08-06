<template>
  <div id="app">
    <div class="app-wrapper">
      <div class="home">
        <header-menu class="header-menu" />
        <dashboard class="dashboard" />
      </div>
      <sidebar class="sidebar" />
    </div>
  </div>
</template>

<script>
import HeaderMenu from "./components/header/HeaderMenu.vue";
import dashboard from "./components/dashboard/dashboard.vue";
import sidebar from "./components/sidebar/sidebar.vue";
export default {
  name: "App",
  components: {
    HeaderMenu,
    dashboard,
    sidebar,
  },
};
</script>

<style>
* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}
#app {
  display: flex;
  justify-content: center;
  align-items: center;
  width: 100%;
  height: 100%;
  min-width: 1336px;
}
.app-wrapper {
  display: flex;
  border: 15px solid #fdd9d9;
  box-shadow: 1px 1px 120px #fdd9d9;
  border-radius: 50px;
  overflow: hidden;
  flex-direction: row;
  width: 90%;
  margin-top: 5%;
  margin-bottom: 5%;
}
.home {
  width: 70%;
  height: calc(100% - 160px);
  display: flex;
  flex-direction: column;
  justify-content: space-between;
}
.header-menu {
  width: 90%;
  margin: 30px auto;
  height: 100px;
  /* background: red; */
}
.dashboard {
  width: 90%;
  margin: 0 auto;
}
.sidebar {
  width: 30%;
}
</style>
