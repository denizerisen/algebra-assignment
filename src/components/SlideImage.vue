<template>
  <div class="slide__column--right">
        <img class="img__circle--yellow" src="../assets/yellow-circle.svg" />
        <img class="slide__image" src="../assets/mountain-image.png" alt="mountain image">
        <img class="img__circle--pink" src="../assets/image-background.svg" width="100%" />
        
  </div>
</template>

<script lang="ts">
    import {Component, Vue} from 'vue-property-decorator';

    @Component
    export default class SlideImage extends Vue { 
       
    }

</script>

<style lang="sass">
    .img__circle--yellow
        position: absolute
        right: 0
        top: 0
        width: 250px
    .img__circle--pink
        position: absolute
        right: 0.75em
        top: 70px
        width: 500px
        z-index: 1
    .slide__image
        position: absolute
        top: 160px
        right: 55px
        border-radius: 50%
        z-index: 3
        width: 425px

</style>