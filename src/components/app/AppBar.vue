<template>
  <v-toolbar  fixed :elevation="0" class="align-centre"  style="border-bottom: 1px solid black; background-color: white;">
    <!-- Mobile Hamburger Menu Icon -->
    <v-app-bar-nav-icon
      v-if="!$vuetify.display.mdAndUp"
      @click="drawer = !drawer"
    ></v-app-bar-nav-icon>

    <!-- Toolbar Title -->
    <v-toolbar-title>
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
    </v-toolbar-title>

    <!-- Desktop Navigation Buttons -->
    <div v-if="$vuetify.display.mdAndUp" class="ml-auto">
      <v-btn
        v-for="item in menu"
        :key="item"
        class="text-body-1 blue-grey-darken-4"
        :href="`#${item.toLowerCase()}`"
        variant="text"
      >
        {{ item }}
      </v-btn>
    </div>

    <!-- Mobile Navigation Drawer -->
    <v-navigation-drawer
      v-model="drawer"
      app
      temporary
      right
    >
      <v-list>
        <v-list-item
          v-for="item in menu"
          :key="item"
          :href="`#${item.toLowerCase()}`"
          @click="drawer = false"
        >
          <v-list-item-title>{{ item }}</v-list-item-title>
        </v-list-item>
      </v-list>
    </v-navigation-drawer>
  </v-toolbar>
</template>

<script setup>
import { ref } from 'vue';

const drawer = ref(false); // State for the navigation drawer
const menu = [
  'Home',
  'About',
  'Applications',
  'Products',
  'ContactUs',
];
</script>
