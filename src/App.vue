<template>

<v-app>
    
    <v-app-bar
      app
    >
      
    <v-flex justify-center>
      <v-btn
        color="primary"
        text
        to="/"
      >
        <span class="mlr-3">Home</span>
      </v-btn>

      <v-btn
        color="primary"
        text
        to="/about"
      >
        <span class="mlr-3">About Me</span>
      </v-btn>

      <v-btn
        color="primary"
        text
        to="/resume"
      >
        <span class="mlr-3">Resume</span>
      </v-btn>

      <v-btn
        color="primary"
        text
        to="/blog"
      >
        <span class="mlr-3">Blog</span>
      </v-btn>

      <v-btn
        color="primary"
        text
        to="/contact"
      >
        <span class="mlr-3">Contact Me</span>
      </v-btn>
    
    </v-flex>
      
      <!--
      <v-btn
        href="https://github.com/amattioli7"
        target="_blank"
        color="primary"
        
      >
        <span class="mr-2">Check out my GitHub Repository!</span>
        <v-icon color="white">mdi-open-in-new</v-icon>
      </v-btn>
      -->
    </v-app-bar>

  <div id="app">
    <div id="nav">
      <router-link to="/"></router-link>
      <router-link to="/about"></router-link>
      <router-link to="/resume"></router-link>
      <router-link to="/blog"></router-link>
      <router-link to="/contact"></router-link>
    </div>
    <router-view/>
  </div>

</v-app>

</template>

<style lang="scss">
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  background-image: url("assets/Background Pattern.png");
  background-size: 500px;
  background-repeat: repeat;
}

#nav {
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
