<script>

import { store } from '../store.js'
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
          <div class="card-container w-100">
            <appSingleCard v-for="(card, index) in store.allCards" :key="index" :myCardName="card.name" :myCardImage="card.card_images[0].image_url" :myCardArchetype="card.archetype" />
          </div>
        </div>
      </div>
    </div>
  </main>
</template>

<style lang="scss" scoped>
  main {
    height: calc(100% - 75px);
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
        display: flex;
        flex-wrap: wrap;    
      }
    }
  }


</style>
