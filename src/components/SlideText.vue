<template>
  <div class="slide__left">
    <div class="header">
    <img  src="../assets/header-text-background.svg" width="100%"/>
    <h1 class="slide__header">{{headerText}}</h1>
    </div>
    <h2 class="slide__subheader">{{this.subheaderText}}</h2>
    <p class="slide__text">{{this.text}}</p>
  
    <input type="text" class="input" v-model="headerText"/>
    <input type="text" class="input" v-model="subheaderText"/>
    <input type="text" class="input" v-model="text"/>
  </div>
</template>

<script lang="ts">
    import {Component, Vue} from 'vue-property-decorator';

    @Component
    export default class SlideText extends Vue { 
        headerText: string = 'Lorem ipsum dolor sit amet, consectetur adipiscing'
        subheaderText: string = 'Lorem ipsum dolor sit amet, consectetur adipiscing'
        text: string = 'Lorem ipsum dolor sit amet, consectetur adipiscing elit. Nulla dignissim sagittis diam in molesite. Morbi vulputate volutpat massa, ut tincidunt nunc convallisa. Suspendisse dapibus diam sit amet nisl gravida. '
    }

</script>

<style lang="sass">
    .slide__left
        font-family: 'Chewy', cursive
        color: white
        margin-top: 60px
        padding: 1em
        text-align: center
        align-self: center
        justify-self: center
        width: 80%
    .header
        max-height: 170px
    .slide__header, .slide__subheader
        font-weight: 100
    .slide__header
        font-size: 3.5em
        line-height: 1
        transform: translateY(100%) translateY(-5.2em)
        
    .slide__subheader
        font-size: 35px
        margin: 0
        padding: 0 10px
    .slide__text
        font-family: 'Gaegu', cursive
        text-align: left
        margin-top: 2em
        padding-right: 15px
        line-height: 1
        font-size: 28px
</style>