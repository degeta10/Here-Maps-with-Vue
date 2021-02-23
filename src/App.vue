<template>
  <div id="app">
    <HereMap :center="center" :apiKey="apiKey" />
  </div>
</template>

<script>
import HereMap from "./components/HereMap";

export default {
  name: "App",
  components: {
    HereMap,
  },
  data() {
    return {
      center: {
        lat: 40.73061,
        lng: -73.935242,
      },
      apiKey: process.env.VUE_APP_HERE_MAPS_API_KEY,
      width: "100",
      height: "100",
      zoom: "10",
    };
  },
};
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
