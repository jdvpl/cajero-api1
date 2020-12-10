<template>
  <div id="app">
    <div class="header">
      <div>
        <Menu></Menu>
      </div>
    </div>

    <div class="main-component text-center">
      <jumbotrom></jumbotrom>

    </div>

    <!-- usuario -->

    <div class="m-auto">
       
    </div>
    <div class="footer">
      <div class="d-flex bg-dark text-light align-items-center px-3 py-3">
        <strong class="m-auto">Desarrollado por: Juan Daniel Suarez</strong>
      </div>
    </div>
  </div>
</template>

😁
<script>

import Jumbotrom from './components/Jumbotrom.vue';
import Menu from './components/Menu.vue';
export default {
  name: "App",
  components: {
    Jumbotrom,
    Menu
  }
};
</script>

<style>
body {
  margin: 0 0 0 0;
}

nav {
  background-color: rgba(0, 0, 0, 0.521) !important;
}
.footer {
  bottom: 0;
  position: fixed;
  width: 100%;
  text-align: center !important;
}
</style>
