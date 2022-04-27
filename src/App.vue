<template>
  <div>
    <nav class="navbar navbar-expand-lg navbar-dark bg-dark">
      <div class="container">
          <a class="navbar-brand" href="">MKT</a>
          <button class="navbar-toggler" type="button" data-bs-toggle="collapse" data-bs-target="#navbarTogglerDemo02" aria-controls="navbarTogglerDemo02" aria-expanded="false" aria-label="Toggle navigation">
              <span class="navbar-toggler-icon"></span>
          </button>
          <div class="collapse navbar-collapse">
              <ul class="navbar-nav ms-auto">
                  <li class="nav-item">
                      <a class="nav-link" href="">Home</a>
                  </li>
                  <li class="nav-item">
                      <a class="nav-link" href="">About</a>
                  </li>
                  <li class="nav-item">
                      <a class="nav-link" href="">Works</a>
                  </li>
              </ul>
          </div>
      </div>
    </nav>
  <HomePage/>
  <AboutPage/>
  <FindMe/>
  </div>
</template>

<script>
import HomePage from './components/Home.vue'
import AboutPage from './components/About.vue'
import FindMe from './components/FindMe.vue'

export default {
  name: 'App',
  components: {
    HomePage, AboutPage, FindMe
  }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  /* text-align: center; */
  color: #2c3e50;
  /* margin-top: 60px; */
  background-color: #1c1c1c;
}
.navbar  {
  cursor: pointer;
  position: fixed;
}
</style>
