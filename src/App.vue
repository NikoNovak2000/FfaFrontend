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
           <table class="table table-hover"> 
            <thead> 
                <th scope="coll">Naziv </th>
                <th scope="coll">Cijena </th>
                <th scope="coll">Slika </th>
                <th scope="coll">Kolicina </th>

            </thead>
            <tbody>
                <tr>
                  <td>Baconburger </td>
                  <td> 8$ </td>
                  <td><img src="../public/Images/Burgers/Baconburger.jpg" height="100" class="d-inline-block align-top" alt=""
                            loading="lazy" /> </td>
                  <td> 1 </td>
                </tr>

                <tr>
                  <td>Kebab </td>
                  <td> 6$ </td>
                  <td><img src="../public/Images/Kebab/Kebab.jpg" height="100" class="d-inline-block align-top" alt=""
                            loading="lazy" /> </td>
                  <td> 1 </td>
                </tr>

                <tr>
                  <td>Pizza Mexicana </td>
                  <td> 10$ </td>
                  <td><img src="../public/Images/Pizza/PizzaMexicana.jpg" height="100" class="d-inline-block align-top" alt=""
                            loading="lazy" /> </td>
                  <td> 1 </td>
                </tr>

                <tr>
                  <td>Fried Calamari </td>
                  <td> 15$ </td>
                  <td><img src="../public/Images/Seafood/FriedCalamari.jpg" height="100" class="d-inline-block align-top" alt=""
                            loading="lazy" /> </td>
                  <td> 1 </td>
                </tr>
              </tbody>
              </table>
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