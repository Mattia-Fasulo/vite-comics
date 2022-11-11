<template>
    <main>

    </main>
    <SectionMenu />


</template>

<script>
import SectionMenu from './SectionMenu.vue';
export default {
    components: {
        SectionMenu
    },
    name: 'MainComponent'
}
</script>

<style lang="scss" scoped>
@use '../assets/styles/partials/mixins' as *;
@use '../assets/styles/partials/variables' as *;

main {
    @include center();
    color: white;
    background-color: black;
    height: 140px;
}
</style>