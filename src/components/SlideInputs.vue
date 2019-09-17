<template>
  <div class="slide__inputs">
    <div class="slide__input__column">
      <input
        type="text"
        name="title"
        placeholder="Title"
        v-bind:class="[!isTitleValid && isTitleValid!==null ? 'invalid' : 'slide__input']"
        maxlength="55"
        v-on:input="inputChangedHandler($event)"
      />
      <p v-show="!isTitleValid && isTitleValid!==null" class="invalid-feedback">{{errors.title}}</p>
    </div>
    <div class="slide__input__column">
      <input
        type="text"
        name="subtitle"
        placeholder="Subtitle"
        class="slide__input"
        maxlength="55"
        v-on:input="inputChangedHandler($event)"
      />
    </div>
    <div class="slide__input__column">
      <input
        type="text"
        name="bodyText"
        placeholder="Body Text"
        class="slide__input"
        maxlength="55"
        v-on:input="inputChangedHandler($event)"
      />
    </div>
  </div>
</template>

<script lang="ts">
import { Component, Vue } from 'vue-property-decorator';

@Component
export default class SlideInputs extends Vue {
  errors = {
    title: '',
  };
  isTitleValid: any = null;
  inputChangedHandler(event: object) {
    this.validateForm(event);
    this.$emit('getText', event);
  }

  validateForm(event: any) {
    switch (event.target.name) {
      case 'title':
        this.isTitleValid = event.target.value.length > 0;
        this.errors.title = this.isTitleValid ? '' : 'Title can not be empty';
        break;
      default:
        break;
    }
  }
}
</script>

<style lang="sass">
  .slide__inputs
    width: 100%
    background: $lightgrey
    margin: 0 auto
    display: flex
  .slide__input__column
    margin: auto
  .slide__input, .invalid
    margin: 1em auto
    padding: .375rem .75rem
    border-radius: 2px
    +font($font-gaegu, 200)
    font-size: 30px
  .slide__input
    border: 1px solid black
  .invalid
    border: 2px solid $lightred
    margin-bottom: .3em
  .invalid-feedback
    +font($font-mono, 100)
    display: block
    margin: 0
    color: $lightred
    font-size: 16px

</style>