<template>
<head>
</head>
  <div id="app">
    <div class="container">
      <div class="row">
        <div class="col">
          <nav class="navbar navbar-expand-lg bg-light">
            <div class="container-fluid">
              <button class="navbar-toggler" type="button" data-bs-toggle="collapse"
                  data-bs-target="#navbarSupportedContent" aria-controls="navbarSupportedContent" aria-expanded="false"
                  aria-label="Toggle navigation">
                <span class="navbar-toggler-icon"></span>
                  </button>
                    <div class="collapse navbar-collapse" id="navbarSupportedContent">
                      <h1>Aplikacija brze hrane</h1>
                      <a class="navbar-brand" href="#">
                        <img src="../public/Images/brzicheese.jpg" height="100" class="d-inline-block align-top" alt=""
                          loading="lazy" />
                        </a>
                          <ul class="navbar-nav mr-auto mt-2 mt-lg-0">
                            <li class="nav-item">
                              <router-link to="/" class="nav-link">Početna</router-link>
                            </li>
                            <li class="nav-item">
                              <router-link to="/" class="nav-link">Kosarica</router-link>
                            </li>
                             <li class="nav-item">
                              <router-link to="/" class="nav-link">O applikaciji</router-link>
                            </li>
                             <li class="nav-item">
                              <router-link to="/" class="nav-link">Neki link</router-link>
                            </li>
                          </ul>
              </div>
            </div>
          </nav>
           
        </div>
          <div class="container">
          <router-view />
          <!-- tu router dinamicki ubaci screen -->
          </div>
      </div>
    </div>

  </div>
</template>
<style lang="scss">
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}
nav {
  padding: 30px;
  a {
    font-weight: bold;
    color: #2c3e50;
    &.router-link-exact-active {
      color: #42b983;
    }
  }
}
</style>