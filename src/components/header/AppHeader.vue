<script>
// import

export default {

  name: "AppHeader",
};

</script>



<template>

    <header>

        <img src="../../assets/img/logo.png" alt="">

        <h1>Yu-Gi-Oh Api</h1>
        
    </header>
  

</template>



<style lang="scss" scoped>
@use "../../styles/partials/variables" as *;
@use "../../styles/partials/mixins" as *;


header{
    display: flex;
    align-items: center;
    img{
        width: 200px;   
    }
}


</style>