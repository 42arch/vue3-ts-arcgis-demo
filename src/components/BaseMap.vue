<template>
  <div class="map" id="map">
    <slot></slot>
  </div>
</template>

<script lang="ts">
import TileLayer from '@arcgis/core/layers/TileLayer'
import MapView from '@arcgis/core/views/MapView'
import Map from '@arcgis/core/Map'

import { defineComponent, onMounted } from 'vue'

export default defineComponent({
  setup() {

    function loadBaseMap() {
      const tileLayer = new TileLayer({
        url: 'https://services.arcgisonline.com/arcgis/rest/services/Canvas/World_Dark_Gray_Base/MapServer'
      })

      const map = new Map({
        layers: [tileLayer]
      })

      const view = new MapView({
        map: map,
        center: [120, 32],
        zoom: 7,
        container: "map"
      })
    }
    
    onMounted(() => {
      loadBaseMap()
    })

    return {}
  },
})
</script>

<style scoped>
#map {
  padding: 0;
  margin: 0;
  height: 100%;
  width: 100%;
}

a {
  color: #42b983;
}

</style>