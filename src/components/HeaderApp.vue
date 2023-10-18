<template>

  <div class="age-increase">
    <h1> V-on:click @click </h1>
    {{ title }} - {{ author }} - {{ age }}
    <button @click="age++"> Increase the age </button>
    <button @click="age--"> Decrease the age </button>
    <button @click="resetage"> Reset the age </button>
  </div>

</template>

<script>

export default {
  name: 'HeaderComponent',

  data() {
    return {
      title: 'This is a Book',
      author: 'Mehdi',
      age: 26,
      defaultage: 26
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

  .age-increase {
    display: flex;
    flex-direction: column;
    width: 500px;
    height: 300px;
    margin: 20px 50px 20px 40px;
    border: 1px solid black;
    padding: 30px;
  }

</style>
