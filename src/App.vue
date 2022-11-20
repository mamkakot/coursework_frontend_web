<template>
  <v-app :theme="theme">
    <v-app-bar>
      <v-spacer></v-spacer>

      <v-btn
          :prepend-icon="theme === 'light' ? 'mdi-weather-sunny' : 'mdi-weather-night'"
          @click="onClick"
      >Toggle Theme
      </v-btn>
    </v-app-bar>

    <v-main>
      <v-container>
        <RoomsList></RoomsList>
      </v-container>
    </v-main>
  </v-app>
</template>

<script>

// import ChoresList from "@/components/ChoresList";
import {ref} from 'vue'
import RoomsList from "@/components/RoomsList";


export default {
  name: 'App',
  components: {
    RoomsList
  },
  setup() {
    const theme = ref('light')

    function onClick() {
      theme.value = theme.value === 'light' ? 'dark' : 'light'
    }

    return {theme, onClick}
  }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
