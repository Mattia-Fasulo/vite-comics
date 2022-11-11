

<template>
  <HeaderComponent />
  <MainComponent />
  <FooterComponent />
</template>

<script >

import MainComponent from './components/MainComponent.vue';
import FooterComponent from './components/FooterComponent.vue';
import HeaderComponent from './components/HeaderComponent.vue';
export default {
  components: {
    HeaderComponent,
    FooterComponent,
    MainComponent
  }

}

</script>

<style lang="scss" scoped>
@use './assets/styles/partials/mixins' as *;
@use './assets/styles/partials/variables' as *;
</style>
