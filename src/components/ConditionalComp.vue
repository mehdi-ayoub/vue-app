<template>
  <div class="age-increase">
    <h1> Conditional Directive V-if </h1>
    <button class="show-button">
      Show the Content
    </button>

    <div class="second-component">
      {{ title }} - {{ author }} - {{ age }}
      <button @click="age++"> Increase the age </button>
      <button @click="age--"> Decrease the age </button>
      <button @click="resetage"> Reset the age </button>
    </div>
  </div>
</template>

<script>
export default {

  name: 'ConditionalDirective',

  data() {

    return {
      title: 'This Book for V-if Directive ',
      author: ' Vue . js',
      age: 500,
      defaultage: 500
    }
  },
  methods: {
    resetage() {
      this.age = this.defaultage
    }
  }
}
</script>

<style>
  .show-button {
    width: 200px;
    margin-bottom: 30px;
  }

  .second-component {
    display: flex;
    flex-direction: column;
  }
</style>
