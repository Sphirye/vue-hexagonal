<script lang="ts">
import Vue from 'vue';
// Uncomment import and local "components" registration if library is not registered globally.
import { VueHexagonal } from '@/entry.esm';

export default Vue.extend({
  name: 'ServeDev',
  components: {
    VueHexagonal,
  }
});
</script>

<template>
  <div id="app">
    <VueHexagonal width="200px" height="200px" img="https://static.wikia.nocookie.net/cookierun/images/c/c1/Starfruit_Cookie.png"/>
  </div>
</template>
