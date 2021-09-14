<template>
  <v-app>
    <v-app-bar
      app
      color="black"
      dense
    >

      <v-toolbar-title color="white">Adam Mattioli's Personal Website</v-toolbar-title>

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
      <HelloWorld/>
    </v-main>
  </v-app>
</template>

<script>
import HelloWorld from './components/HelloWorld';

export default {
  name: 'App',

  components: {
    HelloWorld,
  },

  data: () => ({
    //
  }),
};
</script>
