<script setup>
import AppLayout from '@/components/layout/AppLayout.vue'
import RegisterForm from '@/components/auth/RegisterForm.vue'
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
              <v-divider class="my-4"></v-divider>

              <RegisterForm></RegisterForm>

              <v-divider class="my-4"></v-divider>
            </v-card-text>
          </v-card>
        </v-col>
      </v-row>
    </template>
  </AppLayout>
</template>
