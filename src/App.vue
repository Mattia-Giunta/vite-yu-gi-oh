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
    this.getArchetype()
  },

  methods: {

    getCard() {

      store.loading = true

      store.apiUrl = 'https://db.ygoprodeck.com/api/v7/cardinfo.php?num=50&offset=0';

      if(store.selectValue){

        store.apiUrl = `https://db.ygoprodeck.com/api/v7/cardinfo.php?archetype=${store.selectValue}`;

      };

      axios.get(store.apiUrl)

       .then( response => { 

        store.cardList = response.data.data;

        store.loading = false

      });
    },

    getArchetype() {

      axios.get(store.apiUrlArchetype)

       .then( response => { 

        store.arrayArchetype = response.data;

      });
    },

  },

};

</script>



<template>
  
  <AppHeader/>

  <main>

    <AppSearch @searchArch="getCard" />

    <CardList/>

  </main>
  

</template>



<style lang="scss">

@use "./styles/general.scss";


main{
  background-color: #D48F38;
  
}

</style>
