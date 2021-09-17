<template>
<v-layout
align-center
justify-center
>
  <div class="contact">
    <h1 class="mt-4">Contact Me:</h1>

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
        
    </v-card>

  </div>
</v-layout>
</template>