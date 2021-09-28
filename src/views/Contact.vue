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
          v-model="name"
          ref="name"
          placeholder="Name"
          clearable
          clear-icon="mdi-close-circle"
          >
          </v-text-field>

          <v-text-field
          v-model="email"
          ref="email"
          placeholder="Email Address"
          clearable
          clear-icon="mdi-close-circle"
          >
          </v-text-field>

          <v-text-field
          v-model="subject"
          ref="subject"
          placeholder="Subject"
          clearable
          clear-icon="mdi-close-circle"
          >
          </v-text-field>

          <v-textarea
          v-model="message"
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

  data() {
    return{
      name: '',
      email: '',
      subject: '',
      message: '',
    }
  },
  
  methods: {
    sendEmail(){

      var data = {
        service_id: 'service_0vaf75q',
        template_id: 'template_o9kklme',
        user_id: 'user_8ty7iCF1VLUoYxPSqDXaQ',
        template_params: {
          user_name: this.name,
          user_email: this.email,
          subject: this.subject,
          message: this.message,
        }
      }

      //console.log(data)
      
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