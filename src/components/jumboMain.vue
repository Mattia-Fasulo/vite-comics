<template>
    <div class="jumbo">

    </div>
</template>

<script>
export default {
    name: "JumboMain",

}
</script>

<style lang="scss" scoped>
@use '../assets/styles/partials/mixins' as *;
@use '../assets/styles/partials/variables' as *;

.jumbo {
    height: 390px;
    background: url('/img/jumbotron.jpg');
    background-position-x: center;
    background-size: cover;


}
</style>