<template>
  <img alt="Vue logo" src="./assets/logo.png">

  <head>
    <title>leaflet-map-simple</title>
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <meta charset="utf-8">
  </head>

  <body>
    <Map />
  </body>
</template>

<script>
import Map from './components/Map.vue'
import 'leaflet/dist/leaflet.css'
import 'leaflet/dist/leaflet.js'

export default {
  name: 'App',
  components: {
    Map
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

body {
  margin: 0;
  padding: 0;
}

#map {
  position: absolute;
  top: 0;
  bottom: 0;
  right: 0;
  left: 0;
}

#map-title {
  position: relative;
  margin-top: 10px;
  margin-left: 50px;
  float: left;
  background: white;
  border: 2px solid rgba(0, 0, 0, 0.2);
  padding: 6px 8px;
  font-family: Helvetica;
  font-weight: bold;
  font-size: 24px;
  z-index: 800;
}
</style>
