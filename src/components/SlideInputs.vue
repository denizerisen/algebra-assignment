<template>
  <div class="slide__inputs">
        <input type="text" name="headerText" class="slide__input" maxlength="55" v-on:input="inputChangedHandler($event)"/>
        <input type="text" name="subheaderText" class="slide__input" maxlength="55" v-on:input="inputChangedHandler($event)"/>
        <input type="text" name="text" class="slide__input" maxlength="55" v-on:input="inputChangedHandler($event)"/>
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


<style>

</style>