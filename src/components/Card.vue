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
    flex-basis: calc((100% - 70px) / 6);
    height: 300px;
    padding: 10px;

    .card-img {
        overflow: hidden;
        height: 200px;
        object-fit: cover;

        img {
            object-fit: cover;
        }
    }

    h4 {
        padding: 15px 0;
        text-transform: uppercase;
        font-size: 0.8rem;
        font-weight: 300;
    }


}

@media screen and (max-width: 1100px) {
    .card {
        flex-basis: calc((100% - 70px) / 5);
    }
}

@media screen and (max-width: 992px) {
    .card {
        flex-basis: calc((100% - 70px) / 4);
    }
}

@media screen and (max-width: 769px) {
    .card {
        flex-basis: calc((100% - 70px) / 3);
    }
}

@media screen and (max-width: 570px) {
    .card {
        flex-basis: calc((100% - 70px) / 2);
    }
}

@media screen and (max-width: 470px) {
    .card {
        h4 {
            text-align: center;
        }

        .card-img {
            text-align: center;
        }

        flex-basis: 100%;
    }
}
</style>