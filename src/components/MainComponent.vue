<template>

    <JumboMain />

    <CurrentSeries />

    <SectionMenu />

</template>

<script>
import JumboMain from './JumboMain.vue';
import SectionMenu from './SectionMenu.vue';
import CurrentSeries from './CurrentSeries.vue';
export default {
    components: {
        SectionMenu,
        JumboMain,
        CurrentSeries
    },
    name: 'MainComponent'
}
</script>

<style lang="scss" scoped>
@use '../assets/styles/partials/mixins' as *;
@use '../assets/styles/partials/variables' as *;
</style>