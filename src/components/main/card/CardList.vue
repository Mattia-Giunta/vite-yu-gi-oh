<script>
// import
import CardChild from './CardChild.vue';
import { store } from "../../../store";

export default {

  name: "CardList",

  components:{

    CardChild,
    
  },

  data() {

    return {

      store,
    };
  },
};

</script>



<template>
  
    <section>

      <div class="count-container">

        <span >Found {{store.cardList.length}} cards</span>

      </div>

      <span class="loader" v-if=" ( store.loading ) "></span>

      <div >

        <figure>

          <CardChild v-for="(element,index) in store.cardList" 
            :key="index"
            :propsElement="element" 
          />

        </figure>


      </div>


    </section>


</template>



<style lang="scss" scoped>
@use "../../../styles/partials/variables" as *;
@use "../../../styles/partials/mixins" as *;

section{

  width: 80%;
  height: 750px;
  margin: 0 auto;
  padding: 30px;
  background-color: #212529;
  overflow: auto;

  .count-container{

    background-color: #212529;
    padding: 20px 10px;
    color: white;

    span{

      font-weight: bold;

    }

  }

  figure{

    display: flex;
    flex-wrap: wrap;
    gap: 20px;
    justify-content: space-between;
   
  }

}


.loader {
  color: black;
  font-size: 20px;
  width: 1em;
  height: 1em;
  border-radius: 50%;
  position: relative;
  left: 50%;
  text-indent: -9999em;
  animation: mulShdSpin 1.3s infinite linear;
  transform: translateZ(0);
  
}

@keyframes mulShdSpin {
  0%,
  100% {
    box-shadow: 0 -3em 0 0.2em, 
    2em -2em 0 0em, 3em 0 0 -1em, 
    2em 2em 0 -1em, 0 3em 0 -1em, 
    -2em 2em 0 -1em, -3em 0 0 -1em, 
    -2em -2em 0 0;
  }
  12.5% {
    box-shadow: 0 -3em 0 0, 2em -2em 0 0.2em, 
    3em 0 0 0, 2em 2em 0 -1em, 0 3em 0 -1em, 
    -2em 2em 0 -1em, -3em 0 0 -1em, 
    -2em -2em 0 -1em;
  }
  25% {
    box-shadow: 0 -3em 0 -0.5em, 
    2em -2em 0 0, 3em 0 0 0.2em, 
    2em 2em 0 0, 0 3em 0 -1em, 
    -2em 2em 0 -1em, -3em 0 0 -1em, 
    -2em -2em 0 -1em;
  }
  37.5% {
    box-shadow: 0 -3em 0 -1em, 2em -2em 0 -1em,
     3em 0em 0 0, 2em 2em 0 0.2em, 0 3em 0 0em, 
     -2em 2em 0 -1em, -3em 0em 0 -1em, -2em -2em 0 -1em;
  }
  50% {
    box-shadow: 0 -3em 0 -1em, 2em -2em 0 -1em,
     3em 0 0 -1em, 2em 2em 0 0em, 0 3em 0 0.2em, 
     -2em 2em 0 0, -3em 0em 0 -1em, -2em -2em 0 -1em;
  }
  62.5% {
    box-shadow: 0 -3em 0 -1em, 2em -2em 0 -1em,
     3em 0 0 -1em, 2em 2em 0 -1em, 0 3em 0 0, 
     -2em 2em 0 0.2em, -3em 0 0 0, -2em -2em 0 -1em;
  }
  75% {
    box-shadow: 0em -3em 0 -1em, 2em -2em 0 -1em, 
    3em 0em 0 -1em, 2em 2em 0 -1em, 0 3em 0 -1em, 
    -2em 2em 0 0, -3em 0em 0 0.2em, -2em -2em 0 0;
  }
  87.5% {
    box-shadow: 0em -3em 0 0, 2em -2em 0 -1em, 
    3em 0 0 -1em, 2em 2em 0 -1em, 0 3em 0 -1em, 
    -2em 2em 0 0, -3em 0em 0 0, -2em -2em 0 0.2em;
  }
}
  


</style>
