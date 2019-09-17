<template>
  <div class="slide__inputs">
    <input type="text" name="title" placeholder="Title" class="slide__input" maxlength="55" v-on:input="inputChangedHandler($event)"/>
    <input type="text" name="subtitle" placeholder="Subtitle" class="slide__input" maxlength="55" v-on:input="inputChangedHandler($event)"/>
    <input type="text" name="bodyText" placeholder="Body Text" class="slide__input" maxlength="55" v-on:input="inputChangedHandler($event)"/>
  </div>
</template>

<script lang="ts">
import { Component, Vue } from 'vue-property-decorator';

@Component
export default class SlideInputs extends Vue {
    inputChangedHandler(value: object) {
        this.$emit('getText', value)
    }
}
</script>

<style lang="sass">
  .slide__inputs
    width: 100%
    background: $lightgrey
    margin: 0 auto
    display: flex
    
  .slide__input
    width: 25%
    margin: 1em auto
    padding: .375rem .75rem
    border: 1px solid black
    border-radius: 2px
    +font($font-gaegu, 200)
    font-size: 30px

</style>