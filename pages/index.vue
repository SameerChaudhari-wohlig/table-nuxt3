<template>
  <v-app :theme="theme">
    <v-app-bar title="Table" elevation="11" flat>
      <v-btn
        :prepend-icon="
          theme === 
'light' ? 'mdi-weather-sunny' : 'mdi-weather-night'
        "
        @click="onClick"
        >Dark Mode</v-btn
      >
    </v-app-bar>
    <v-main>
 <tab/>
    </v-main>
  </v-app>
</template>
<script setup>
import { ref } from "vue";

const theme = ref("light");

function onClick() {
  theme.value = theme.value === "light" ? "dark" : "light";
}
</script>

<style></style>
