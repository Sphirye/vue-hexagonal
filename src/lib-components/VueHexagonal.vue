<template>
  <div :class="`vue-hexagon-container ${ outlined != undefined ? 'outlined' : '' }`">
    <div :class="`vue-hexagon`" :style="`width: ${width}; height: ${height}; ${ img != undefined ? 'background-image: url('+img+');' : '' }`">
      <span>{{text}}</span>
    </div>
  </div>
</template>

<script lang="ts">
import { Component, Prop, Vue } from "vue-property-decorator"

@Component({ name: 'VueHexagonal' })
export default class VueHexagonal extends Vue {

  @Prop() readonly text: string | undefined
  @Prop() readonly img: string | undefined
  @Prop({ default: '50px' }) readonly width: string | undefined
  @Prop({ default: '50px' }) readonly height: string | undefined
  @Prop({ default: '50px' }) readonly transparent: string | undefined
  @Prop() readonly outlined?: any | undefined

}
</script>

<style>
div.vue-hexagon-container {
  display: inline-block;
  -webkit-clip-path: polygon(50% 0, 100% 38%, 81% 100%, 19% 100%, 0 38%);
  clip-path: polygon(50% 0, 100% 38%, 81% 100%, 19% 100%, 0 38%);
}

.vue-hexagon-container .vue-hexagon {
  display: flex;
  justify-content: center;
  align-items: center;
  background: rgb(206, 206, 206);

  background-size: cover;
  background-position: center;

  -webkit-clip-path: polygon(50% 0, 100% 38%, 81% 100%, 19% 100%, 0 38%);
  clip-path: polygon(50% 0, 100% 38%, 81% 100%, 19% 100%, 0 38%);
  margin: 3px;
}

.outlined {
  background-color: black;
}

</style>
