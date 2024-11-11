<script setup>
import { ref } from 'vue'

// Define separate refs for password and password confirmation visibility
const passwordVisible = ref(false)
const confirmPasswordVisible = ref(false)
</script>

<template>
  <v-form fast-fail @submit.prevent>
    <v-text-field
      density="compact"
      placeholder="First Name"
      prepend-inner-icon="mdi-account-box-edit-outline"
      variant="outlined"
      label="First Name"
    ></v-text-field>

    <v-text-field
      label="Last name"
      variant="outlined"
      density="compact"
      prepend-inner-icon="mdi-account-box-edit-outline"
    ></v-text-field>

    <v-text-field
      label="Email"
      variant="outlined"
      placeholder="Email Address"
      prepend-inner-icon="mdi-email-outline"
    ></v-text-field>

    <!-- Password Field -->
    <v-text-field
      :append-inner-icon="passwordVisible ? 'mdi-eye-off' : 'mdi-eye'"
      :type="passwordVisible ? 'text' : 'password'"
      density="compact"
      placeholder="Enter your password"
      prepend-inner-icon="mdi-lock-outline"
      variant="outlined"
      @click:append-inner="passwordVisible = !passwordVisible"
      label="Password"
    ></v-text-field>

    <!-- Password Confirmation Field -->
    <v-text-field
      label="Password Confirmation"
      :append-inner-icon="confirmPasswordVisible ? 'mdi-eye-off' : 'mdi-eye'"
      :type="confirmPasswordVisible ? 'text' : 'password'"
      density="compact"
      placeholder="Confirm your password"
      prepend-inner-icon="mdi-lock-outline"
      variant="outlined"
      @click:append-inner="confirmPasswordVisible = !confirmPasswordVisible"
    ></v-text-field>

    <v-btn
      class="mt-2 bg-primary"
      type="submit"
      block
      prepend-icon="mdi-account-plus-outline"
    >
      Register
    </v-btn>

    <v-divider class="my-4"></v-divider>
    <h5 class="text-center">
      Already have an account? Click here to
      <router-link to="/login" class="text-primary"> Login </router-link>
    </h5>
  </v-form>
</template>
