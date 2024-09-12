<script>
/* 
    Per importare ed utilizzare un componente dentro un altro devo SEMPRE seguire questi 3 passi:
    1) Importazione del componente
    2) Dichiarazione del componente
    3) Utilizzo del componente
*/

import axios from 'axios';

export default {
  data() {
    return {
      
    }
  },
  components: {
    
  },
  created() {
    axios
      .get('URL')
      .then()
  }
}
</script>

<!-- All'interno del template ci va un solo elemento -->
<template> 
  <div>
    
  </div>
</template>

<style lang="scss" scoped>
// Import all of Bootstrap's CSS
@import "~bootstrap/scss/bootstrap";
</style>
