<template>
  <div class="slide__left">
    <div class="header">
        <img  src="../assets/header-text-background.svg" width="100%"/>
        <h1 class="slide__header">{{headerText}}</h1>
    </div>
    <h2 class="slide__subheader">{{subheaderText}}</h2>
    <p class="slide__text">{{text}}</p>
  </div>
</template>

<script lang="ts">
    import {Component, Vue, Prop} from 'vue-property-decorator';

    @Component
    export default class SlideText extends Vue { 
        @Prop(String)
        headerText;

        @Prop(String)
        subheaderText;

        @Prop(String)
        text;
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