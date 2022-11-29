<template>
  <v-app class="app">
    <v-main>
      <router-view />
    </v-main>
  </v-app>
</template>
<style scoped>
.app {
  background-color: rgb(255, 255, 255);
}
</style>
<script>
import "./css/index.css";
export default {
  name: "App",

  data: () => ({
    //
  }),
};
</script>
