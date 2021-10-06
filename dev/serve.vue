<script lang="ts">
import Vue from 'vue'
import { VueHexagonal } from '@/entry.esm'

export default Vue.extend({
  name: 'ServeDev',
  components: {
    VueHexagonal,
  }
});
</script>

<template>
  <div id="app">
    <VueHexagonal heptagon outlined width="200px" height="250px" img="https://static.wikia.nocookie.net/cookierun/images/c/c1/Starfruit_Cookie.png"/>
  </div>
</template>
