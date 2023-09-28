<template>
  <div id="map-title">EDIT map title</div>
  <div id="map"></div>
</template>

<script>
import L from 'leaflet'
export default {
  name: 'HelloWorld',
  props: {
    msg: String
  },
  mounted(){
    const map = L.map('map', {
        center: [21.5, -79], // EDIT coordinates to re-center map
        zoom: 6,  // EDIT from 1 (zoomed out) to 18 (zoomed in)
        scrollWheelZoom: false
      })
      L.tileLayer(
        'https://{s}.basemaps.cartocdn.com/light_all/{z}/{x}/{y}{r}.png', {
          attribution: '&copy <a href="https://osm.org/copyright">\
            OpenStreetMap</a> contributors, &copy\
            <a href="https://carto.com/attribution">CARTO</a>'
      }).addTo(map)
      
      /* Display a point marker with pop-up text */
      L.marker([41.77, -72.69]).addTo(map) // EDIT marker coordinates
      .bindPopup("Insert pop-up text here") // EDIT pop-up text message
    
  }
}

  /* display basemap tiles -- see others at https://leaflet-extras.github.io/leaflet-providers/preview/ */
</script>


<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
h3 {
  margin: 40px 0 0;
}
ul {
  list-style-type: none;
  padding: 0;
}
li {
  display: inline-block;
  margin: 0 10px;
}
a {
  color: #42b983;
}
</style>
