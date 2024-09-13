<script>
/* 
    Per importare ed utilizzare un componente dentro un altro devo SEMPRE seguire questi 3 passi:
    1) Importazione del componente
    2) Dichiarazione del componente
    3) Utilizzo del componente
*/

import { store } from '../store.js'

export default {
    data() {
        return {
            store
        }
    },
    props: {
        myCardImage: String,
        myCardArchetype: String,
        myCardName: String
    },
    components: {
        
    }
}
</script>

<!-- All'interno del template ci va un solo elemento -->
<template> 
    <div class="single-card d-flex flex-wrap">
        <div class="card-img">
            <img :src="myCardImage" :alt="myCardName">
        </div>
        <div class="card-info">
            <h3 class="card-name text-center">
                {{  myCardName }}
            </h3>
            <h4 class="card-type text-center">
                {{ myCardArchetype }}
            </h4>
        </div>
    </div>
</template>

<style lang="scss" scoped>
@use '../assets/scss/partials/mixins.scss' as *;
@use '../assets/scss/partials/variables.scss' as *;

.single-card {
    display: flex;
    flex-direction: column;
    align-items: center;
    width: calc((100% / 4) - 15px);
    height: 500px;

    .card-img {
        display: flex;
        justify-content: center;
        img {
            height: 350px;
            
        }
    }
}

</style>