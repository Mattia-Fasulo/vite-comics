

<template>
  <HeaderComponent />
  <main>

    content goes here

  </main>
  <div class="component">


  </div>
  <FooterComponent />
</template>

<script >

import FooterComponent from './components/FooterComponent.vue';
import HeaderComponent from './components/HeaderComponent.vue';
export default {
  components: {
    HeaderComponent,
    FooterComponent
  }

}

</script>

<style lang="scss" scoped>
@use './assets/styles/partials/mixins' as *;
@use './assets/styles/partials/variables' as *;

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
