<template>
  <BaseMap />
</template>

<script lang="ts">
import { defineComponent } from 'vue'
import BaseMap from './components/BaseMap.vue'

export default defineComponent({
  name: 'App',
  components: {
    BaseMap
  }
})
</script>

<style>
@import "https://js.arcgis.com/4.19/@arcgis/core/assets/esri/themes/light/main.css";

#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  width: 100%;
  height: 100%;
  padding: 0;
  margin: 0;
  user-select: none;
}
</style>
