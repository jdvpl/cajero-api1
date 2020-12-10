<template>
  <div id="app">
    <div class="header">
      <div>
        <b-navbar toggleable="sm" type="dark" variant="dark">
          <b-navbar-toggle target="nav-text-collapse"></b-navbar-toggle>
          <b-navbar-brand class="font-weight-bold mr-5"
            >Cajero Api</b-navbar-brand
          >
          <b-collapse id="nav-text-collapse" is-nav>
            <b-navbar-nav class="text-center">
              <b-nav-item v-on:click="init" v-if="is_auth">Inicio</b-nav-item>
              <b-nav-item v-on:click="getBalance" v-if="is_auth">Saldo</b-nav-item>
              <b-nav-item v-if="is_auth">Transaccion</b-nav-item>
              <b-nav-item v-if="is_auth">Cerrar Sesion</b-nav-item>
            </b-navbar-nav>
          </b-collapse>
        </b-navbar>
      </div>
    </div>

    <div class="main-component text-center">
      <jumbotrom></jumbotrom>

    </div>

    <!-- usuario -->

    <div class="m-auto">
        <b-form class="w-50 m-auto">

          <label class="sr-only" for="inline-form-input-name">Nombre</label>
          <b-input-group prepend="👤" class="mb-2 mr-sm-2 mb-sm-0 sm-12">
            <b-form-input
            type="text"
              id="inline-form-input-username"
              placeholder="Juan Daniel Suarez"
            ></b-form-input>
          </b-input-group><br>
          <label class="sr-only" for="inline-form-input-username"
            >Correo</label
          >
          <b-input-group prepend="✉" class="mb-2 mr-sm-2 mb-sm-0">
            <b-form-input
            type="email"
              id="inline-form-input-username"
              placeholder="jdvpl@gmail.com"
            ></b-form-input>
          </b-input-group><br>

          <b-input-group prepend="🔑" class="mb-2 mr-sm-2 mb-sm-0">
            <b-form-input
            type="password"
              id="inline-form-input-username"
              placeholder="Contraseña"
            ></b-form-input>
          </b-input-group><br>
          <b-button variant="dark" class="btn btn-block">Guardar</b-button>
        </b-form>
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
export default {
  name: "App",
  components: {
    Jumbotrom
  },
  data: function () {
    return {
      is_auth: localStorage.getItem("isAuth") || false,
    };
  },
  methods: {},
    beforeCreate: function () {
    localStorage.setItem("current_username", "JDVPL");
    localStorage.setItem("isAuth", true);
  },
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
