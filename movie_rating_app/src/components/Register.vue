<template>
  <v-form v-model="valid"
          ref="form"
          lazy-validation>
    <v-text-field label="Name"
                  v-model="name"
                  required></v-text-field>
    <v-text-field label="Email"
                  v-model="email"
                  :rules="emailRules"
                  required></v-text-field>
    <v-text-field label="Password"
                  v-model="password"
                  required></v-text-field>
    <v-text-field name="input-7-1"
                  label="Confirm Password"
                  v-model="confirm_password"></v-text-field>
    <v-btn @click="submit"
           :disabled="!valid">
      submit
    </v-btn>
    <v-btn @click="clear">clear</v-btn>
  </v-form>
</template>
