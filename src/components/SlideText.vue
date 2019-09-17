<template>
  <div class="slide__column--left">
    <div class="slide__title__area">
        <img  src="../assets/header-title-background.svg" width="100%"/>
        <h1 class="slide__title__area__title">{{title}}</h1>
    </div>
    <h2 class="slide__subtitle">{{subtitle}}</h2>
    <p class="slide__bodytext">{{bodyText}}</p>
  </div>
</template>

<script lang="ts">
    import {Component, Vue, Prop} from 'vue-property-decorator';

    @Component
    export default class SlideText extends Vue { 
        @Prop(String)
        title;

        @Prop(String)
        subtitle;

        @Prop(String)
        bodyText;
    }
</script>

<style lang="sass">
    .slide__column--left
        font-family: 'Chewy', cursive
        color: white
        margin-top: 60px
        padding-left: 100px
        text-align: center
        align-self: center
        justify-self: center
        width: 100%

    .slide__title__area
        max-height: 170px

    .slide__title, .slide__subtitle
        font-weight: 100

    .slide__title__area__title
        font-size: 3.4em
        line-height: 1
        padding: 0 15px
        transform: translateY(100%) translateY(-5.2em)
        height: 110px
        
    .slide__subtitle
        font-size: 35px
        margin: 0
        padding: 0 10px

    .slide__bodytext
        +font($font-gaegu, 100)
        text-align: left
        margin-top: 2em
        padding-right: 15px
        line-height: 1
        font-size: 28px
</style>