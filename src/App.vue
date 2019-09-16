<template>
  <div id="app" class="grid">
    <SlideText/>
    <SlideImage/>
  </div>
</template>

<script lang="ts">
import { Component, Vue } from 'vue-property-decorator';
import SlideText from './components/SlideText.vue';
import SlideImage from './components/SlideImage.vue';

@Component({
  components: {
    SlideText,
    SlideImage
  },
})
export default class App extends Vue {}
</script>

<style lang="sass">
  @import 'sass/main.sass'
  body
    margin: 0
    background: $lilac
  #app
    font-family: 'Avenir', Helvetica, Arial, sans-serif
    -webkit-font-smoothing: antialiased
    -moz-osx-font-smoothing: grayscale
    max-width: 1440px
  .grid
    display: grid
    grid-template-columns: 60% 40%
    width: 100vw
</style>
