<script setup>
import AppLayout from '@/components/layout/AppLayout.vue'
import LoginForm from '@/components/auth/LoginForm.vue'
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
            image="/images/bg-card-favicon.jfif"
            variant="outlined"
            elevation="20"
          >
            <v-card-title class="text-center">
              <v-img
                class="mx-auto"
                src="/images/logo-favicon.png"
                :width="mobile ? '75%' : '25%'"
              ></v-img>
              <h3 class="font-weight-black">Welcome to Lost and Found</h3>
              <p>Login Form</p>
            </v-card-title>
            <v-card-text class="bg-surface-light pt-4">
              <v-divider class="my-4"></v-divider>

              <LoginForm></LoginForm>

              <v-divider class="my-4"></v-divider>
              <h5 class="text-center">
                Don't have account? Click here to
                <router-link to="/register" class="text-primary">
                  Register
                </router-link>
              </h5>
            </v-card-text>
          </v-card>
        </v-col>
      </v-row>
    </template>
  </AppLayout>
</template>
