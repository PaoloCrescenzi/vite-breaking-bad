<script>
// This starter template is using Vue 3 <script setup> SFCs
// Check out https://vuejs.org/api/sfc-script-setup.html#script-setup
import NavBar from './components/NavBar.vue';
import DropDown from './components/DropDown.vue';
import CardCont from './components/CardCont.vue';

import axios from 'axios';

import { store } from './store';

export default {
  components : {
    NavBar, DropDown, CardCont
  },
  data() {
    return {
      store
    }
  },
  mounted : function() {
    
    axios.get('https://swapi.dev/api/people/')
    .then((res) => {
      console.log(res.data.results);
      this.store.cardList = res.data.results;
    })
    .catch((err) => {
      console.log('errore', err);
    });
  }
}
</script>

<template>
  <NavBar/>
  <DropDown/>
  <CardCont/>
</template>

<style scoped>
  
</style>
