<template>
    <main>

    </main>
    <div class="component">

    </div>
</template>

<script>
export default {
    name: 'MainComponent'
}
</script>

<style lang="scss" scoped>
@use '../../assets/styles/partials/mixins' as *;
@use '../../assets/styles/partials/variables' as *;

main {
    @include center();
    color: white;
    background-color: black;
    height: 140px;
}

.component {
    background-color: $blu;
    height: 160px;
}
</style>