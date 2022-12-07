<script>
  import axios from "axios";

  export default{
    name: "SingleCard",
    data () {
      return{

      };
    },
    props : {
      character : Object
    }
  }
</script>

<template>  
  <div class="card" style="width: 18rem;">
    <img class="card-img-top" :src="`${character.image}`" alt="">
    <div class="card-body">
      <h5 class="card-title">{{character.name}}</h5>
      <p>{{character.species}}</p>
    </div>
  </div>
</template>

<style scoped>

</style>