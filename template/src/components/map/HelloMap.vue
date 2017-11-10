<template>
  <div id="map">
    <div class="wrapper">
      <v-map :zoom="zoom" :center="center">
        <v-tilelayer :url="url" :attribution="attribution"></v-tilelayer>
        <v-marker :lat-lng="marker"></v-marker>
      </v-map>
    </div>
  </div>
</template>

<script>
  import Vue2Leaflet from 'vue2-leaflet'
  import L from 'leaflet'

  export default {
    name: 'example',
    components: {
      'v-map': Vue2Leaflet.Map,
      'v-tilelayer': Vue2Leaflet.TileLayer,
      'v-marker': Vue2Leaflet.Marker
    },
    data () {
      return {
        zoom: 5,
        center: L.latLng(47.00, 2.349014),
        url: 'http://{s}.tile.osm.org/{z}/{x}/{y}.png',
        attribution: '&copy; <a href="http://osm.org/copyright">OpenStreetMap</a> contributors',
        marker: L.latLng(47.00, 2.349014)
      }
    }
  }
</script>

<style>
  @import "~leaflet/dist/leaflet.css";

  #map {
    height: 100%;
    padding: 20px;
  }

  div.wrapper {
    height: 100%;
    -webkit-box-shadow: 0 4px 8px 0 rgba(0, 0, 0, 0.2), 0 6px 20px 0 rgba(0, 0, 0, 0.19);
    -moz-box-shadow: 0 4px 8px 0 rgba(0, 0, 0, 0.2), 0 6px 20px 0 rgba(0, 0, 0, 0.19);
    box-shadow: 0 4px 8px 0 rgba(0, 0, 0, 0.2), 0 6px 20px 0 rgba(0, 0, 0, 0.19);
  }

  v-map {
    margin: 20px;
    height: 100%;
  }
</style>
