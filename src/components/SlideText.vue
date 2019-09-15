<template>
  <div class="slide__left">
    <h1 class="slide__header">{{this.headerText}}</h1>
    <h2 class="slide__subheader">{{this.headerText}}</h2>
    <p class="slide__text">{{this.headerText}}</p>
  
  </div>
</template>

<script lang="ts">
    import {Component, Vue} from 'vue-property-decorator';

    @Component
    export default class SlideText extends Vue { 
        headerText: string = 'Lorem ipsum dolor sit amet, consectetur adipiscing'
        subheaderText: string = 'Lorem ipsum dolor sit amet, consectetur adipiscing'
        text: string = 'Lorem ipsum dolor sit amet, consectetur adipiscing elit.  Nulla dignissi vulputate volutpat massa, ut tincidunt nunc convallis a. Suspendisse dapibus diam sit amet nisl gravida. '
    }

</script>

<style lang="sass">
    .slide__header
        background: no-repeat url(../assets/header-text-background.svg)
</style>