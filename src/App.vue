<script>
/* 
    Per importare ed utilizzare un componente dentro un altro devo SEMPRE seguire questi 3 passi:
    1) Importazione del componente
    2) Dichiarazione del componente
    3) Utilizzo del componente
*/

import axios from 'axios';
import { store } from './store.js';
import AppHeader from '../src/components/appHeader.vue';
import AppMain from '../src/components/appMain.vue';



export default {
  data() {
    return {
      store
    }
  },
  components: {
    AppHeader,
    AppMain,
    
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
    },
  }

</script>

<!-- All'interno del template ci va un solo elemento -->
<template> 
  <div>
    <AppHeader />
    <AppMain />
  </div>
</template>

<style lang="scss">
  // Import all of Bootstrap's CSS
  @import "bootstrap/scss/bootstrap";
</style>
