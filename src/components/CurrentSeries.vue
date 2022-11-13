<template>
    <div class="current-series">
        <div class="title-current-series">
            <h2>Current series</h2>
        </div>
        <div class="container row">

            <Card v-for="(item, index) in cards" :key="index" :obj="item" />

        </div>
        <div class="container row">
            <button type="button" class="btn-current-series">Load More</button>
        </div>
    </div>
</template>

<script>
import { comics } from '../data/links';
import Card from './Card.vue';
export default {
    name: "CurrentSeries",
    components: {
        Card
    },
    data() {
        return {
            cards: comics
        }
    }
}
</script>

<style lang="scss" >
@use '../assets/styles/partials/mixins' as *;
@use '../assets/styles/partials/variables' as *;


.current-series {
    position: relative;
    padding: 50px 0 40px;
    color: white;
    background-color: black;
    min-height: 140px;
    height: max-content;
}

.title-current-series {
    position: absolute;
    top: -25px;
    left: 175px;
    padding: 10px;
    background-color: $blu;
    text-transform: uppercase;
}


.row {
    @include center();
    padding-top: 0px;
    flex-flow: row wrap;


}

.btn-current-series {
    cursor: pointer;
    width: 200px;
    color: white;
    font-weight: 600;
    padding: 10px;
    background-color: $blu;
    text-transform: uppercase;
}


@media screen and (max-width: 769px) {
    .title-current-series {
        left: 75px;
    }
}
</style>