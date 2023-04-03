<template>
<head>
    <link rel="stylesheet" href="//fonts.googleapis.com/css?family=Roboto:400,500,700,400italic|Material+Icons">
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
                       <a class="navbar-brand" href="#">
                        <img src="../public/Images/brzicheese.jpg" height="100" class="d-inline-block align-top" alt=""
                          loading="lazy" />
                        </a> 
                          <ul class="navbar-nav mr-auto mt-2 mt-lg-0">
                            <li class="nav-item">
                              <router-link to="/" class="nav-link">Home</router-link>
                            </li>
                              <li class="nav-item">
                               <router-link to="/cart" class="nav-link">Cart</router-link>
                              </li>
                          </ul>

                <form class="d-flex" role="search">
                  <input class="form-control me-2" type="search" placeholder="Search" aria-label="Search">
                  <button class="btn btn-outline-success" type="submit">Search</button>
                </form>
              </div>
            </div>
          </nav>
        </div>
      </div>
    </div>

    <div class="container">
      <router-view />
      <!-- tu router dinamicki ubaci screen -->
    </div>

  </div>
</template>

<script>
import { defineComponent } from '@vue/composition-api'

export default defineComponent({
  setup() {
    
  },
})
</script>

<style lang="scss">
  body {
    background-color: rgba(var(--b3f, 250, 250, 250), 1);
  }

  #app {
    font-family: 'Avenir', Helvetica, Arial, sans-serif;
    -webkit-font-smoothing: antialiased;
    -moz-osx-font-smoothing: grayscale;
    text-align: center;
    color: #2c3e50;
  }

  #nav {
    padding: 30px;
    background-color: white;
    border-bottom: #ccc 1px solid;
    margin-bottom: 30px;

    a {
      font-weight: bold;
      color: #2c3e50;

      &.router-link-exact-active {
        color: #42b983;
      }
    }
  }
</style>