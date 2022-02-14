<template>
  <div id="app">
   
   
    <nav class="navbar" role="navigation" aria-label="main navigation" >
  <div class="navbar-brand">
    <a class="navbar-item">
      <img src="https://bulma.io/images/bulma-logo.png" width="112" height="28">
    </a>

    <a role="button" class="navbar-burger" aria-label="menu" aria-expanded="false" data-target="navbarBasicExample">
      <span aria-hidden="true"></span>
      <span aria-hidden="true"></span>
      <span aria-hidden="true"></span>
    </a>
  </div>

  <div id="navbarBasicExample" class="navbar-menu">
    <div class="navbar-start">
     

      <a class="navbar-item">
      <router-link to="/" >Home</router-link> |
      </a>
         <a class="navbar-item">
      <router-link to="/about">About</router-link> |
      </a>   <a class="navbar-item">
      <router-link to="/contact">Contact Us</router-link> |
      </a>

      <div class="navbar-item has-dropdown is-hoverable">
        <a class="navbar-link">
       DestinationDetails
        </a>
    
        <div class="navbar-dropdown">
          <div v-for="destination in destinations" :key="destination.name">
          <a class="navbar-item">
             <router-link
          :to="{
            name: 'DestinationDetails',
            params: { slug: destination.slug }
          }"
        >
          <h2>{{ destination.name }}</h2>
        </router-link>
         <router-link
            :to="{
              name: 'DestinationDetails',
              params: { slug: destination.slug }
            }"
          >
            
          </router-link>
        
          </a>
          </div>
        </div>
      </div>
    </div>

    <div class="navbar-end">
      <div class="navbar-item">
        <div class="buttons">
          <a class="button is-primary">
            <strong><router-link to="/signup"> Sign up</router-link></strong>
          </a>
        <a class="button is-primary">
            <strong><router-link to="/login "> Login</router-link></strong>
          </a>
        </div>
      </div>
    </div>
  </div>
</nav>
<router-view />
<footer class="footer">
  <div class="content has-text-centered">
    <p>
      <strong>Demo App</strong> by Koshal Garg The source code is licensed
      <a href="http://opensource.org/licenses/mit-license.php">MIT</a>. The website content
      is licensed <a href="http://creativecommons.org/licenses/by-nc-sa/4.0/">CC BY NC SA 4.0</a>.
    </p>
  </div>
</footer>
  </div>
  
  
</template>
<script>

import store from "./store.js";



export default {
  name: "home",
  components: {},
  data() {
    return {
      destinations: store.destinations
    };
  }
};
</script>

<style scoped>
@import "https://cdn.jsdelivr.net/npm/bulma@0.9.3/css/bulma.min.css"; 

/* 
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}

#nav {
  padding: 30px;
}

#nav a {
  font-weight: bold;
  color: #2c3e50;
}

#nav a.router-link-exact-active {
  color: #42b983;
} */
</style>
