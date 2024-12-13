<template>
  <v-app-bar :elevation="0" style="border-bottom: 1px solid black">
    <template #title>
      <div class="d-inline-flex align-center text-h4 font-weight-bold my-5 text-primary">
        <v-img
          src="/favicon.ico"
          alt="Logo"
          width="40"
          height="40"
          class="mr-2"
        />
        HEMANT TRADERS
      </div>
    </template>
    <template v-if="$vuetify.display.mdAndUp" #append>
      <div class="hidden-sm-and-down">
        <v-btn v-for="item in menu" :key="item" class="text-body-1 blue-grey-darken-4" :href="`#${item.toLowerCase()}`"
          variant="text">
          {{ item }}
        </v-btn>
      </div>
    </template>
  </v-app-bar>
</template>

<script setup>
const menu = [
  'Home',
  'About',
  'Testimonials',
  'Work',
  'Team',
  'Features',
  'ContactUs'
]
</script>
