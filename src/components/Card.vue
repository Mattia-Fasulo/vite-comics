<template>
    <div class="card">
        <div class="card-img">
            <img :src="obj.thumb" :alt="obj.series">
        </div>
        <h4>{{ obj.series }}</h4>
    </div>
</template>

<script>
export default {
    name: "Card",
    props: ["obj"]


}
</script>

<style lang="scss" scoped>
@use '../assets/styles/partials/mixins' as *;
@use '../assets/styles/partials/variables' as *;

.card {
    flex-basis: calc((100% - 130px) / 6);
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
</style>