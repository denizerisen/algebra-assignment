<template>
  <div class="slide__right">
        <img class="first" src="../assets/yellow-circle.svg" />
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
        background-color: $test
        position: absolute
        right: 0
        top: 0
    .second
        position: relative
        z-index: 2
</style>