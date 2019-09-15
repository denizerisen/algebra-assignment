<template>
  <div id="app">
    <SlideText/>
  </div>
</template>

<script lang="ts">
import { Component, Vue } from 'vue-property-decorator';
import SlideText from './components/SlideText.vue';

@Component({
  components: {
    SlideText,
  },
})
export default class App extends Vue {}
</script>

<style lang="sass">
  @import 'sass/main.sass'
  #app
    font-family: 'Avenir', Helvetica, Arial, sans-serif
    -webkit-font-smoothing: antialiased
    -moz-osx-font-smoothing: grayscale
    background: $lilac

</style>
