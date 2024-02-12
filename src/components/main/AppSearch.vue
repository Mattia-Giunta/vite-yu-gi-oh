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

    <select v-model="store.selectValue" name="" id="">

      <option 
      :value="element.archetype_name"
      v-for="(element,index) in store.arrayArchetype"
      :key="index"
      >{{ element.archetype_name }}</option>
      

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
