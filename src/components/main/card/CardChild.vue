<script>
// import

export default {
  name: "CardChild",

  props:[
    'propsElement'
  ],

    data() {

        return {

            
        };
    },
};

</script>



<template>


<div class="container-card">
            
    <img :src="propsElement.card_images[0].image_url_small"> 

    <h3>{{propsElement.name}}</h3>

    <p>{{ propsElement.archetype }}</p>
            
</div>
  

</template>



<style lang="scss" scoped>
@use "../../../styles/partials/variables" as *;
@use "../../../styles/partials/mixins" as *;


div{

    width: calc(100% / 5 - 20px);
    background-color: #D48F38;
    text-align: center;
    &:hover{box-shadow: 0px 0px 26px 6px #ccd820;}
    




    img{

        width: 100%;

    }

    h3{

        color: white;
    }

}

</style>
