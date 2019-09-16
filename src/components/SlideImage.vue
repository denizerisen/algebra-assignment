<template>
  <div class="slide__right">
        <img class="first" src="../assets/yellow-circle.svg" />
        <img class="slide__image" src="../assets/mountain-image.png" alt="mountain image">
        <img class="second" src="../assets/image-background.svg" width="100%" />
        
  </div>
</template>

<script lang="ts">
    import {Component, Vue} from 'vue-property-decorator';

    @Component
    export default class SlideImage extends Vue { 
       
    }

</script>

<style lang="sass">
    .first
        position: absolute
        right: 0
        top: 0
        width: 17.5%
    .second
        position: absolute
        right: 0.75em
        width: 35%
        z-index: 1
    .slide__image
        position: absolute
        top: 5em
        right: 3em
        border-radius: 50%
        z-index: 3
        width: 30%

</style>