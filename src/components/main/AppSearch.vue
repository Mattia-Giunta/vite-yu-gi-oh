<script>
// import

export default {
  name: "AppSearch",
};

</script>



<template>
  
  <div>

    <select name="" id="">

      <option value="" disabled hidden>Seleziona Classe</option>

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
