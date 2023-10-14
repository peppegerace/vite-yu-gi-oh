<script>
import { store } from '../../data/store';

export default {
  name: 'ProductCard',
  props: {
    name: String,
    archetype: String,
    image: String,
  },
  // data() {
  //   return {
  //     store
  //   }
  // }
}
</script>


<template>

<div class="col-auto">
  <div class="cardyugi">
    <div class="image">
      <img :src="image" :alt="name">
    </div>
    <div class="description">
      <h3>{{ name }}</h3>
      <span class="archetype">{{ archetype }}</span>
    </div>
  </div>
</div>

</template>


<style lang="scss">

img {
  max-width: 100%;
}


</style>