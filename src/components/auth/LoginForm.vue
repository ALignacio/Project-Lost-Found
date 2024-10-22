<template>
  <v-form fast-fail @submit.prevent>
    <v-text-field label="Username" variant="outlined"></v-text-field>
    <v-text-field
      label="Password"
      variant="outlined"
      type="password"
    ></v-text-field>

    <v-btn class="mt-2 bg-primary" type="submit" block prepend-icon="mdi-login"
      >Login</v-btn
    >
  </v-form>
</template>
