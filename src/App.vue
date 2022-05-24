<template>
  <div id="app">
    <nav class="navbar navbar-expand-lg navbar-light bg-light">
      <div class="container-fluid">
        <a class="navbar-brand" href="#">Navbar</a>
        <div class="collapse navbar-collapse" id="navbarSupportedContent">
          <ul class="navbar-nav me-auto ">
            <li class="nav-item">
              <router-link class="nav-link" :to="{name:'首頁'}">Home</router-link>
            </li>
            <li class="nav-item">
              <router-link class="nav-link" to="/page">Link</router-link>
            </li>
          </ul>
        </div>
      </div>
    </nav>
    <!-- <img src="./assets/logo.png"> -->
    <!-- <HelloWorld/> -->
    <router-view name="menu"></router-view>
    <div class="container">
      <router-view></router-view>
    </div>
  </div>
</template>

<script>
import HelloWorld from './components/HelloWorld'

export default {
  name: 'App',
  components: {
    HelloWorld
  },
  created(){
    const api = `${process.env.APIPATH}/api/${process.env.CUSTOMPATH}/products`
    this.$http.get(api)
    .then((response)=>{
      console.log(response.data)
    })
  }
}
</script>

<style lang="scss">
@import "./assets/all";
</style>
