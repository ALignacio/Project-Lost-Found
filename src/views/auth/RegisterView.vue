<script setup>
import { ref } from 'vue'

const theme = ref('light')

function onClick() {
  theme.value = theme.value === 'light' ? 'dark' : 'light'
}
</script>

<template>
  <v-responsive class="border rounded">
    <v-app :theme="theme">
      <v-app-bar class="px-3">
        <v-spacer></v-spacer>

        <v-btn
          :prepend-icon="
            theme === 'light' ? 'mdi-weather-sunny' : 'mdi-weather-night'
          "
          text="Toggle Theme"
          slim
          @click="onClick"
        ></v-btn>
      </v-app-bar>

      <v-main>
        <v-container>
          <v-row class="d-flex justify-center">
            <v-col cols="12" md="6">
              <v-card
                class="mx-auto"
                prepend-icon="mdi-account-box-plus-outline"
                subtitle="Register Form"
                variant="outlined"
                elevation="20"
              >
                <template v-slot:title>
                  <span class="font-weight-black"
                    >Welcome to Lost and Found</span
                  >
                </template>

                <v-card-text class="bg-surface-light pt-4">
                  <v-form fast-fail @submit.prevent>
                    <v-text-field
                      label="First name"
                      variant="outlined"
                    ></v-text-field>
                    <v-text-field
                      label="Last name"
                      variant="outlined"
                    ></v-text-field>

                    <v-text-field
                      label="Email"
                      variant="outlined"
                    ></v-text-field>
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
                    <v-btn class="mt-2" type="submit" block>Submit</v-btn>
                    <v-divider class="my-4"></v-divider>
                    <h5 class="text-center">
                      Already have account? Click here to
                      <router-link to="/login" class="text-primary">
                        Login
                      </router-link>
                    </h5>
                  </v-form>
                </v-card-text>
              </v-card>
            </v-col>
          </v-row>
        </v-container>
      </v-main>
      <v-footer border app>Copyright All Rights Reserve</v-footer>
    </v-app>
  </v-responsive>
</template>
