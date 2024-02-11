<script>

import AppHeader from "./components/header/AppHeader.vue";
import AppSearch from "./components/main/AppSearch.vue";
import CardList from "./components/main/card/CardList.vue";


import { store } from "./store";

import axios from "axios";

export default {

  components: {
    AppHeader,
    AppSearch,
    CardList,
  },

  data() {

    return {

      store,
    };
  },

  created() {

    this.getCard();
  },

  methods: {

    getCard() {

      store.loading = true

      axios.get(store.apiUrl)

       .then( response => { 

        store.cardList = response.data.data;

        store.loading = false

      });
    },
  },
};

</script>



<template>
  
  <AppHeader/>

  <main>

    <AppSearch />

    <CardList/>

  </main>
  

</template>



<style lang="scss">

@use "./styles/general.scss";


main{
  background-color: #D48F38;
}

</style>
