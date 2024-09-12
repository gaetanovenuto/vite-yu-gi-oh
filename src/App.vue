<script>
/* 
    Per importare ed utilizzare un componente dentro un altro devo SEMPRE seguire questi 3 passi:
    1) Importazione del componente
    2) Dichiarazione del componente
    3) Utilizzo del componente
*/



import AppHeader from '../src/components/appHeader.vue';
import AppMain from '../src/components/appMain.vue';



export default {
  data() {
    return {
      
    }
  },
  components: {
    AppHeader,
    AppMain,
    
  },
  created() {
    
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
