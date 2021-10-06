<template>
  <div 
    :class="` 
      ${ heptagon != undefined ? 'vue-heptagon-container' : 'vue-hexagon-container' }`"

    :style="`
      ${ outlined != undefined ? 'background-color:'+borderColor+';' : '' }`"
  >
    <div
      :class="`
        ${ heptagon != undefined ? 'vue-heptagon' : 'vue-hexagon' }`"

      :style="`
        width: ${width}; 
        height: ${height}; 
        background-color: ${backgroundColor};
        ${ img != undefined ? 'background-image: url('+img+');' : '' }`"
        >
      <span>{{text}}</span>
    </div>
    
  </div>
</template>

<script lang="ts">
import { Component, Prop, Vue } from "vue-property-decorator"

@Component({ name: 'VueHexagonal' })
export default class VueHexagonal extends Vue {

  @Prop() readonly heptagon: any | undefined
  @Prop() readonly text: string | undefined
  @Prop() readonly img: string | undefined
  @Prop({ default: '50px' }) readonly width: string | undefined
  @Prop({ default: '60px' }) readonly height: string | undefined
  @Prop() readonly outlined?: any | undefined
  @Prop({ default: 'black' }) readonly borderColor: string | undefined
  @Prop({ default: 'white' }) readonly backgroundColor: string | undefined


}
</script>

<style>
.vue-hexagon-container div, .vue-heptagon-container div  {
  display: flex;
  justify-content: center;
  align-items: center;
  background: rgb(206, 206, 206);
  background-size: cover;
  background-position: center;
  margin: 3px;
}

.vue-hexagon-container {
  display: inline-block;
  -webkit-clip-path: polygon(50% 0, 100% 38%, 81% 100%, 19% 100%, 0 38%);
  clip-path: polygon(50% 0, 100% 38%, 81% 100%, 19% 100%, 0 38%);
}

.vue-heptagon-container {
  display: inline-block;
  -webkit-clip-path: polygon(50% 0%, 100% 25%, 100% 75%, 50% 100%, 0% 75%, 0% 25%);
  clip-path: polygon(50% 0%, 100% 25%, 100% 75%, 50% 100%, 0% 75%, 0% 25%);
}

.vue-hexagon-container .vue-hexagon {
  -webkit-clip-path: polygon(50% 0, 100% 38%, 81% 100%, 19% 100%, 0 38%);
  clip-path: polygon(50% 0, 100% 38%, 81% 100%, 19% 100%, 0 38%);
}

.vue-heptagon-container .vue-heptagon {
  -webkit-clip-path: polygon(50% 0%, 100% 25%, 100% 75%, 50% 100%, 0% 75%, 0% 25%);
  clip-path: polygon(50% 0%, 100% 25%, 100% 75%, 50% 100%, 0% 75%, 0% 25%);
}
</style>
