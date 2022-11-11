<template>
    <div class="current-series">
        <div class="title-current-series">
            <h2>Current series</h2>
        </div>
        <div class="container row">

            <div class="card" v-for="(game, index) in games" :key="index">
                <div class="card-img">
                    <img :src="game.thumb" :alt="game.series">
                </div>
                <h4>{{ game.series }}</h4>
            </div>




        </div>
    </div>
</template>

<script>
import { cards } from '../data/links';

export default {
    name: "CurrentSeries",
    data() {
        return {
            games: cards
        }
    }
}
</script>

<style lang="scss" scoped>
@use '../assets/styles/partials/mixins' as *;
@use '../assets/styles/partials/variables' as *;


.current-series {
    position: relative;
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
    padding-top: 50px;
    flex-flow: row wrap;

    .card {
        flex-basis: calc((100%) / 6);
        height: 300px;
        padding: 10px;

        .card-img {
            overflow: hidden;
            height: 200px;
        }

        h4 {
            padding: 15px 0;
            text-transform: uppercase;
            font-size: 0.8rem;
            font-weight: 300;
        }
    }
}
</style>