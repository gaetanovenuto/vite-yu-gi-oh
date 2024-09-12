<script>

import axios from 'axios';
import { store } from '../store.js';
import appSingleCard from './appSingleCard.vue';

export default {
  data() {
    return {
      store
    }
  },
  components: {
    appSingleCard
  },
  created() {
    axios
      .get('https://db.ygoprodeck.com/api/v7/cardinfo.php?num=20&offset=0')
      .then((res) => {
        console.log('Risposta API', res);
        console.log('Data della risposta', res.data);
        console.log('Tutte le carte', res.data.data);

        this.store.allCards = res.data.data;
        console.log(this.store.allCards)
      }
    ) 
  }
}
</script>

<!-- All'interno del template ci va un solo elemento -->
<template> 
  <main>
    <div class="container">
      <div class="row">
        <div class="col py-3">
          <select class="form-select" aria-label="Select">
            <option selected>All</option>
            <option value="Alien">Alien</option>
            <option value="Human">Human</option>
            <option value="Robot">Robot</option>
          </select>
        </div>
        <div class="general-container">
          <div class="row cards-found fw-bold text-white d-flex align-items-center px-3">
            Found X cards
          </div>
          <div class="card-container">
            <appSingleCard 
              v-for="(cards, index) in store.allCards" 
              :key="index"
              :singleCard="store.allCards" />
          </div>
        </div>
      </div>
    </div>
  </main>
</template>

<style lang="scss" scoped>
  main {
    height: calc(100vh - 75px);
    width: 100%;
    background-color: $myOrange;

    .form-select {
      width: 150px;

      &:hover {
        cursor: pointer;
      }
    }

    .general-container {
      padding: 50px 75px;
      background-color: white;

      .cards-found {
        height: 75px;
        background-color: black;
        margin: 0;
      }

      .card-container {
        background-color: blue;
        
      }
    }
  }


</style>
