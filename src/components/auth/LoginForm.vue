<script>
export default {
  data: () => ({
    visible: false,
  }),
}
</script>
<template>
  <v-form fast-fail @submit.prevent>
    <v-text-field
      density="compact"
      placeholder="Email address"
      prepend-inner-icon="mdi-email-outline"
      variant="outlined"
      label="Email"
    ></v-text-field>
    <v-text-field
      :append-inner-icon="visible ? 'mdi-eye-off' : 'mdi-eye'"
      :type="visible ? 'text' : 'password'"
      density="compact"
      placeholder="Enter your password"
      prepend-inner-icon="mdi-lock-outline"
      variant="outlined"
      @click:append-inner="visible = !visible"
      label="Password"
    ></v-text-field>

    <v-btn class="mt-2 bg-primary" type="submit" block prepend-icon="mdi-login"
      >Login</v-btn
    >
  </v-form>
</template>
