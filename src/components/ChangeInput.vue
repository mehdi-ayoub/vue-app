<template>

  <div class="age-increase">
    <h1> Change the input Using V-model </h1>
    <input type="text" v-model="text">
    <p> {{ text }} </p>
    <p> Counting : {{ count }} </p>

  </div>
</template>

<script>
export default {
  data() {
    return {
      text: ''
    }
  },

  computed: {
    count() {
      return this.text.length
    }
  }
}
</script>

<style>

</style>
