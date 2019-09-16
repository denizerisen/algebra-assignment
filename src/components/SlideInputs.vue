<template>
  <div class="slide__inputs">
      <input type="text" class="input" v-on:input="inputChangedHandler($event.target.value)"/>
  </div>
</template>

<script lang="js">
export default {
    methods : {
        inputChangedHandler(value){
            this.$emit('getText', value)
        }
    }
}
</script>


<style>

</style>