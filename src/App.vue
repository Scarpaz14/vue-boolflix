<template>
  <div id="app">
    <backroundImage/>
    <HeaderComponent/>
    <MainComponent/>
  </div>
</template>

<script>
import HeaderComponent from './components/blocks/HeaderComponent.vue';
import MainComponent from './components/blocks/MainComponent.vue';
import backroundImage from './components/backgound/backroundImage.vue';

export default {
  name: 'App',
  components: {
    HeaderComponent,
    MainComponent,
    backroundImage
}
}
</script>

<style lang="scss">
@import './assets/style/global.scss';


</style>
