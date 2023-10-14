<script>
import ProductCard from './partials/ProductCard.vue';
import { store } from '../data/store';

export default {
  name: 'Main',
  components: {
    ProductCard
  },
  data() {
    return {
      store
    }
  }
}
</script>


<template>
 
 <main>

  <div class="container">

    <select name="" id="" class="my-3">

    </select>

    <div class="container cards">
      <div class="row mx-auto">

        <ProductCard
          v-for="card in store.cardResults"
          :key="card.id"
          :name="card.name"
          :archetype="card.archetype"
          :image="card.card_images[0].image_url" />

        <!-- <ProductCard />
        <ProductCard />
        <ProductCard />
        <ProductCard />
        <ProductCard />
        <ProductCard />
        <ProductCard /> -->

      </div>
    </div>

  </div>
 </main>
</template>


<style lang="scss">

@use '../scss/main.scss' as *;

main {
  background-color: #d48f38;

  .cards {
    background-color: white;
    padding-top: 50px;

    .cardyugi {
      width: 230px;
      text-align: center;
      margin-bottom: 15px;
      flex-grow: 1;
      .image {
        width: 100%;
      }
      .description {
        background-color: #d48f38;
        padding: 15px;

        h3 {
          color: white;
          text-transform: uppercase;
        }
      }
    }
  }
}

</style>