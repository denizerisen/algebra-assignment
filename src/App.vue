<template>
  <div id="app" >
    <div class="grid">
      <SlideText :title="title" :subtitle="subtitle" :bodyText="bodyText"/>
      <SlideImage/>
    </div>
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
  title: string = 'Lorem ipsum dolor sit amet, consectetur adipiscing';
  subtitle: string = 'Lorem ipsum dolor sit amet, consectetur adipiscing';
  bodyText: string = 'Lorem ipsum dolor sit amet, consectetur adipiscing elit. Nulla dignissim sagittis diam in molesite. Morbi vulputate volutpat massa, ut tincidunt nunc convallisa. Suspendisse dapibus diam sit amet nisl gravida.';

  inputChangedHandler($event: any) {
    switch ($event.target.name) {
      case 'title':
        this.title = $event.target.value;
        break;
      case 'subtitle':
        this.subtitle = $event.target.value;
        break;
      case 'bodyText':
        this.bodyText = $event.target.value;
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
    -webkit-font-smoothing: antialiased
    -moz-osx-font-smoothing: grayscale
    width: 1280px
    height: 720px
  .grid
    display: grid
    grid-template-columns: 50% 50%
    width: 1280px
    height: 720px
    
</style>
