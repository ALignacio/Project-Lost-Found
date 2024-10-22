<script setup>
import AppLayout from '@/components/layout/AppLayout.vue'
import { useDisplay } from 'vuetify'

const { mobile } = useDisplay()
</script>

<template>
  <AppLayout>
    <template #content>
      <v-row class="d-flex justify-center">
        <v-col cols="12" md="6">
          <v-card
            class="mx-auto"
            variant="outlined"
            elevation="20"
            image="/images/bg-card-favicon.jfif"
          >
            <v-card-title class="text-center">
              <v-img
                class="mx-auto"
                src="/images/logo-favicon.png"
                :width="mobile ? '75%' : '25%'"
              ></v-img>
              <h3 class="font-weight-black">Welcome to Lost and Found</h3>
              <p class="font-weight-bold">Registration Form</p>
            </v-card-title>

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
                  <router-link to="/login" class="text-primary">
                    Login
                  </router-link>
                </h5>
              </v-form>
            </v-card-text>
          </v-card>
        </v-col>
      </v-row>
    </template>
  </AppLayout>
</template>
