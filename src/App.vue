<template>
  <div id="app" class="grid">
    <SlideText :text="text"/>
    <SlideImage/>
    <SlideInputs @getText="inputChangedHandler($event)"/>
  </div>
</template>

<script lang="ts">
import { Component, Vue } from 'vue-property-decorator';
import SlideText from './components/SlideText.vue';
import SlideImage from './components/SlideImage.vue';
import SlideInputs from './components/SlideInputs.vue';

@Component({
  components: {
    SlideText,
    SlideImage,
    SlideInputs,
  },
})
export default class App extends Vue {
  text: string = "Lorem ipsum dolor sit amet, consectetur adipiscing";
  inputChangedHandler(text){
    this.text = text;
  }
}
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
    
  .grid
    display: grid
    grid-template-columns: 60% 40%
    width: 100vw
</style>
