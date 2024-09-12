<script>
/* 
    Per importare ed utilizzare un componente dentro un altro devo SEMPRE seguire questi 3 passi:
    1) Importazione del componente
    2) Dichiarazione del componente
    3) Utilizzo del componente
*/

export default {
    data() {
        return {
            
        }
    },
    props: {
        singleCard: Object
    },
    components: {
        
        }
}
</script>

<!-- All'interno del template ci va un solo elemento -->
<template> 
    <div class="single-card">
        <div class="card-img">
            <img :src="singleCard.card_images.image_url" alt="">
        </div>
        <div class="card-info">
            <div class="card-name">
                {{ singleCard.name }}
            </div>
            <div class="card-type">

            </div>
        </div>
    </div>
</template>

<style lang="scss" scoped>
@use '../assets/scss/partials/mixins.scss' as *;
@use '../assets/scss/partials/variables.scss' as *;

main {
    
}

</style>