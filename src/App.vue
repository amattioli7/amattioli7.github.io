<template>
  <v-app>
    <v-app-bar
      app
      color="black"
      dense
    >

      <v-app-bar-nav-icon @click="drawer = true">

        <v-navigation-drawer
          v-model="drawer"
          absolute
          temporary
        >

        <v-list nav>
          <v-list-item-group
          v-model="group"
          active-class="deep-purple--text text--accent-4"
        >
          <v-list-item>
            <v-list-item-icon>
              <v-icon>mdi-home</v-icon>
            </v-list-item-icon>
            <v-list-item-title>Home</v-list-item-title>
          </v-list-item>

          <v-list-item>
            <v-list-item-icon>
              <v-icon>mdi-account</v-icon>
            </v-list-item-icon>
            <v-list-item-title>Account</v-list-item-title>
          </v-list-item>
        </v-list-item-group>
        </v-list>

        </v-navigation-drawer>

      </v-app-bar-nav-icon>

      <v-toolbar-title>Adam Mattioli's Personal Website</v-toolbar-title>

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
