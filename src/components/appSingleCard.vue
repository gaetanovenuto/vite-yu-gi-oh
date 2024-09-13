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
            <div class="card-name text-center">
                {{  myCardName }}
            </div>
            <div class="card-type text-center">
                {{ myCardArchetype }}
            </div>
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
    height: 450px;
    margin: 0;

    .card-img {
        display: flex;
        justify-content: center;
        img {
            height: 300px;
        }
    }

    .card-info {
        padding-top: 15px;
        text-align: center;
        width: 90%;

        .card-name {
            font-weight: 700;
            font-size: 1.1rem;
        }

        .card-type {
            padding-top: 10px;
            font-weight: 500;   
        }
    }
}

</style>