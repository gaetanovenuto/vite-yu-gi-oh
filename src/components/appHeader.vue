<script>

import { store } from '../store.js'

export default {
  data() {
    return {
      store
    }
  }
}
</script>

<!-- All'interno del template ci va un solo elemento -->
<template> 
  <div>
    <header>
        <img src="/img/logo.jpg" alt="Yu-Gi-Oh">
        <div class="title"> 
            Yu-Gi-Oh Api
        </div>
    </header>
  </div>
</template>

<style lang="scss" scoped>
header {
  display: flex;
  align-items: center;
  padding: 10px;
  height: 75px;

  img {
    width: 150px;
  }

  .title {
    margin-left: 20px;
    font-weight: 500;
    font-size: 32px;
  }

}
</style>
