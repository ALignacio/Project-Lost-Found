<template>
  <v-form fast-fail @submit.prevent>
    <v-text-field label="First name" variant="outlined"></v-text-field>

    <v-text-field label="Last name" variant="outlined"></v-text-field>

    <v-text-field label="Email" variant="outlined"></v-text-field>
    <v-text-field
      label="Password"
      variant="outlined"
      type="password"
    ></v-text-field>
    <v-text-field
      label="Password Confirmation"
      variant="outlined"
      type="password"
    ></v-text-field>
    <v-btn
      class="mt-2 bg-primary"
      type="submit"
      block
      prepend-icon="mdi-account-plus-outline"
      >Register</v-btn
    >
    <v-divider class="my-4"></v-divider>
    <h5 class="text-center">
      Already have account? Click here to
      <router-link to="/login" class="text-primary"> Login </router-link>
    </h5>
  </v-form>
</template>
