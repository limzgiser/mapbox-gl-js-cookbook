<template>
  <base-map :map-options="mapOptions" @load="handleMapLoaded"/>
</template>

<script>
import baseMap from '../base-map'
import addTMSLayer from '../../../snippet/service/tms'
export default {
  components: {
    baseMap
  },
  data () {
    return {
      mapOptions: {
        center: [106.30486062690614, 29.56357402345421],
        zoom: 10
      }
    }
  },
  methods: {
    handleMapLoaded (map) {
      addTMSLayer(map)
    }
  }
}
</script>
