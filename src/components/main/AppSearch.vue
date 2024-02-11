<script>
// import
import { store } from "../../store";

export default {
  name: "AppSearch",

  data() {

    return {

      store,
    };
  },
};



</script>



<template>
  
  <div>

    <select v-model="store.searchText" name="" id="">

      <option value="" disabled hidden>Seleziona Classe</option>
      <option value="" >Alien</option>
      <option value="" >Eroe</option>
      <option value="" >Robot</option>

    </select>

  </div>


</template>



<style lang="scss" scoped>
@use "../../styles/partials/variables" as *;
@use "../../styles/partials/mixins" as *;

div{
  width: 80%;
  margin: 0 auto;
  
  select{
    margin-block: 20px;
    padding: 5px;
    border-radius: 10px;
  }
}


</style>
