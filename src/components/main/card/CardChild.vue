<script>
// import

export default {
  name: "CardChild",
};

</script>



<template>

<!-- v-for="(element,index) in store" :key="index" -->
<div >
            
    <img src="https://images.ygoprodeck.com/images/cards_small/34541863.jpg" alt=""> 

    <h3>"A" Cell Breeding Device</h3>

    <p>Alien</p>
            
</div>
  

</template>



<style lang="scss" scoped>
@use "../../../styles/partials/variables" as *;
@use "../../../styles/partials/mixins" as *;


div{

    width: calc(100% / 5 - 20px);
    background-color: #D48F38;
    text-align: center;

    img{

        width: 100%;

    }

    h3{

        color: white;
    }

}

</style>
