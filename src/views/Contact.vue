<template>

  <v-layout
    align-center
    justify-center
  >
    <div class="contact">
      <h1 class="mt-4" id="contactMe">Contact Me:</h1>

      <v-spacer class="mb-4"></v-spacer>

      <v-card
        ref="form"
        min-width="600px"
      >

        <v-card-text>
          <v-text-field
          ref="name"
          placeholder="Name"
          clearable
          clear-icon="mdi-close-circle"
          >
          </v-text-field>

          <v-text-field
          ref="email"
          placeholder="Email Address"
          clearable
          clear-icon="mdi-close-circle"
          >
          </v-text-field>

          <v-text-field
          ref="subject"
          placeholder="Subject"
          clearable
          clear-icon="mdi-close-circle"
          >
          </v-text-field>

          <v-textarea
          ref="message"
          placeholder="Message"
          maxlength="500"
          clearable
          clear-icon="mdi-close-circle"
          >
          </v-textarea>

        </v-card-text>

          <v-btn
            class="mb-4"
            @click="sendEmail()">
            SEND
          </v-btn>
          
      </v-card>

    </div>
  </v-layout>

</template>

<script>
import { defineComponent } from '@vue/composition-api'
import Vue from 'vue'
import axios from 'axios'
import VueAxios from 'vue-axios'

Vue.use(VueAxios, axios)

export default defineComponent({
  setup() {
    
  },
  
  methods: {
    sendEmail(){

      var data = {
        service_id: 'service_0vaf75q',
        template_id: 'template_o9kklme',
        user_id: 'user_8ty7iCF1VLUoYxPSqDXaQ',
        template_params: {
          user_name: 'Test User Name',
          user_email: 'testUserEmail@test.com',
          subject: 'This is a test subject',
          message: 'Hello Adam! This is a test message!',
        }
      }

      Vue.axios.post('https://api.emailjs.com/api/v1.0/email/send', 
      data)
      .then(function (response){
        console.log(response)
      })
      .catch(function (error){
        console.log(error.response)
      })
    
    },
  }

})
</script>

<style>

  #contactMe{
    color: white;
  }

</style>

<!-- background-image: url("../assets/mc.jpg"); -->