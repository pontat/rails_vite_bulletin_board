<template>
  <div>
    <img alt="Vue logo" src="./assets/logo.png" />
    <HelloWorld msg="Hello Vue 3.0 + Vite" />
  </div>
</template>

<script lang="ts">
import axios from 'axios'
import HelloWorld from './components/HelloWorld.vue'
import { baseUrl } from './util/Util'

export default {
  name: 'App',
  components: {
    HelloWorld,
  },
  mounted: async function () {
    await axios.get(`${baseUrl}/health_check`)
  },
}
</script>
