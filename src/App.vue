<script>
import axios from 'axios';
import Header from './components/Header.vue';
import Main from './components/Main.vue';
import { store } from './data/store';


export default {
  name: 'App',
  components: {
    Header,
    Main
  },
  data() {
    return {
      store
    }
  },
  methods: {
    getApi() {
      axios.get(store.apiUrl)
        .then(res => {
          console.log(res.data.data);
          store.cardResults = res.data.data
        })
        .catch(err =>{

        })
    }
  },
  mounted() {
    this.getApi()
  }
}
</script>


<template>

  <Header />
  <Main />

</template>


<style lang="scss">

@use './scss/main.scss';

</style>