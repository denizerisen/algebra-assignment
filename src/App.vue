<template>
  <div id="app" class="grid">
    <SlideText :headerText="headerText" :subheaderText="subheaderText" :text="text"/>
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
  headerText: string = 'Lorem ipsum dolor sit amet, consectetur adipiscing';
  subheaderText: string = 'Lorem ipsum dolor sit amet, consectetur adipiscing';
  text: string = 'Lorem ipsum dolor sit amet, consectetur adipiscing elit. Nulla dignissim sagittis diam in molesite. Morbi vulputate volutpat massa, ut tincidunt nunc convallisa. Suspendisse dapibus diam sit amet nisl gravida. '

  inputChangedHandler($event){
    console.log($event.target.name);
    console.log($event.target.value);
    switch($event.target.name){
      case 'headerText':
        this.headerText = $event.target.value;
        break;
      case 'subheaderText':
        this.subheaderText = $event.target.value;
        break;
      case 'text':
        this.text = $event.target.value;
        break;
    }
    
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
