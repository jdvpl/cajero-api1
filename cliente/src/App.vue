<template>
  <div id="app">
    <div class="header">
      
      <nav class="navbar navbar-expand-lg navbar-light">
        <div class="container">
          <a class="navbar-brand text-white font-weig" href="#">GesDoc</a>
          <button
            class="navbar-toggler"
            type="button"
            data-bs-toggle="collapse"
            data-bs-target="#navbarNav"
            aria-controls="navbarNav"
            aria-expanded="false"
            aria-label="Toggle navigation"
          >
            <span class="navbar-toggler-icon"></span>
          </button>
          <div class="collapse navbar-collapse" id="navbarNav">
            <ul class="navbar-nav">
              <li class="nav-item">
                <a class="nav-link active text-white" aria-current="page" href="#">Home</a>
              </li>
              <li class="nav-item">
                <a class="nav-link text-white" href="#">Features</a>
              </li>
              <li class="nav-item">
                <a class="nav-link text-white" href="#">Pricing</a>
              </li>
            </ul>
          </div>
        </div>
      </nav>
    </div>
    <div class="main-component">
      <div class="collapse" id="navbarToggleExternalContent">
        <div class="bg-dark p-4">
          <h5 class="text-white h4">Collapsed content</h5>
          <span class="text-muted">Toggleable via the navbar brand.</span>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "App",
  components: {},
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

nav{
  background-color: rgba(0, 0, 0, 0.521) !important;

}
</style>
