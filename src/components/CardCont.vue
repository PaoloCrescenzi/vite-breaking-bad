<template>
  <div class="container p-5 mt-3 bg-white">
    <div class="bg-dark p-1">
      <p>Found 62 Cards</p>
    </div>

    <div class="mt-3" v-for="(card, i) in store" >
      <SingleCard>{{ card }}</SingleCard>
    </div>
  </div>

</template>

<script>
  import SingleCard from './SingleCard.vue';

  import { store } from '../store';

  export default {
    name : 'CardCont',
    components : {
      SingleCard
    },
    data : function() {
      return {
        store
      }
    }
  }
</script>

<style scoped>

</style>