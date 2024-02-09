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

      axios
        .get("https://flynn.boolean.careers/exercises/api/random/mail")
        .then((result) => {

          store.randomMail = result.data.response;
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


</style>
