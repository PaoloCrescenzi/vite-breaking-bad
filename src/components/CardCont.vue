<template>
  <div class="container p-5 mt-3 mb-3 bg-white">
    <div class="bg-dark p-2">
      <p class="text-white">Found 12 Cards</p>
    </div>

    <div class="row">
      <div class="mt-3 col-3" v-for="(card, i) in store.cardList">
        <SingleCard :character="card"></SingleCard>
      </div>
    </div>

  </div>

</template>

<script>
import SingleCard from './SingleCard.vue';

import { store } from '../store';

export default {
  name: 'CardCont',
  components: {
    SingleCard
  },
  data: function () {
    return {
      store
    }
  }
}
</script>

<style scoped>

</style>