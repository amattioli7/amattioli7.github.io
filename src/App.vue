<template>
  <v-app>
    
    <v-app-bar
      app
      dark
      dense
    >
      <v-app-bar-title>Adam Mattioli's Personal Website</v-app-bar-title>
      <v-spacer></v-spacer>

      <v-btn
        color="white"
        text
      >
        <span class="mlr-3">Home</span>
      </v-btn>

      <v-text>|</v-text>

      <v-btn
        color="white"
        text
      >
        <span class="mlr-3">About Me</span>
      </v-btn>

      <v-text>|</v-text>

      <v-btn
        color="white"
        text
      >
        <span class="mlr-3">Resume</span>
      </v-btn>

      <v-text>|</v-text>

      <v-btn
        color="white"
        text
      >
        <span class="mlr-3">Blog</span>
      </v-btn>

      <v-text>|</v-text>

      <v-btn
        color="white"
        text
      >
        <span class="mlr-3">Contact Me</span>
      </v-btn>

      <v-spacer></v-spacer>

      <v-btn
        href="https://github.com/amattioli7"
        target="_blank"
        color="white"
        text
      >
        <span class="mr-2">Check out my GitHub Repository!</span>
        <v-icon color="white">mdi-open-in-new</v-icon>
      </v-btn>
    </v-app-bar>

    <v-main>
      <Home/>
    </v-main>
  </v-app>
</template>

<script>
import Home from './components/Home';

export default {
  name: 'App',

  components: {
    Home,
  },

  data: () => ({
    //
  }),
};
</script>
