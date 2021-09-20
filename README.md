# vue-hexagonal-container

A Hexagonal Vue Component.

# Installation
**NPM**:

    npm i --save-dev vue-hexagonal

**Mount:**

```js
//main.js
import  Vue  from  'vue';
import  VueHexagonal  from  '@sphirye/vue-hexagonal-container';

Vue.use(VueHexagonal);
```

Then in your view/component:

```vue
<template>
  <VueHexagonal/>
</template>

<script>
  import { VueHexagonal } from  '@sphirye/vue-hexagonal';

  export default {
    components: { VueHexagonal }
  }
</script>
```
# Usage

There's 5 props that vue-hexagonal-container can handle:

 - `img`
 - `outlined`
 - `width`
 - `height`
 - `text`

## Images 

Use `img` prop to pass image sources to the component.

```vue
<VueHexagonal img="https://static.wikia.nocookie.net/cookierun/images/c/c1/Starfruit_Cookie.png"/>
```

## Outlined

Use `outlined` prop to draw a outline around the hexagon component.
```vue
<VueHexagonal outlined/>
```
## Width and Height

Use `Width` and `Height` props to handle the hexagon component size.

## Text

Use `text` prop to display text in the hexagon component.

```vue
<VueHexagonal text="sus"/>
```
