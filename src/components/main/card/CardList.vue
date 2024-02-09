<script>
// import
import CardChild from './CardChild.vue';

export default {
    
  name: "CardList",

  components:{
    CardChild,
  }
};

</script>



<template>
  
  <CardChild/>

</template>



<style lang="scss" scoped>
@use "../../../styles/partials/variables" as *;
@use "../../../styles/partials/mixins" as *;


</style>
