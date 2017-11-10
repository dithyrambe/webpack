<template>
  <div class="hello">
    <h1>{{ msg }}</h1>
    <hello-map></hello-map>
  </div>
</template>

<script>
  import Map from './map/HelloMap.vue'

  export default {
    name: 'HelloWorld',
    components: {
      'hello-map': Map
    },
    data () {
      return {
        msg: 'Welcome to Your Vue.js & Leaflet App'
      }
    }
  }
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
  .hello{
    height: 100%;
    display: flex;
    flex-direction: column;
  }

  h1, h2 {
    font-weight: normal;
  }
</style>
