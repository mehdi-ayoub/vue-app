<template>

<div class="age-increase">
  <h1> Conditional and toggling the title </h1>

  <button @click="showcontents">
    <span v-if="showcontent"> Hide Content </span>
    <span v-else> Show Content </span>
  </button>

  <div class="below-content" v-if="showcontent" >
    {{ title }} - {{ author }} - {{ age }}
    <button @click="increaseage"> Increase The age  </button>
    <button @click="decraseage"> Decrease The age </button>
    <button @click="toggleTitle"> Change Title </button>
  </div>

</div>

</template>

<script>
export default {

  data() {
    return {
      title: 'This Book Talks about conditionals',
      alternativetitle: 'This title changed',
      author: 'Mehdi Ayoub',
      age: 32,
      showcontent: true,
    }
  },



  methods: {
    increaseage() {
      this.age++
    },

    decraseage() {
      this.age--
    },

    showcontents() {
      this.showcontent = !this.showcontent
    },

    toggleTitle() {
      if (this.title === 'This Book Talks about conditionals'){
        this.title = this.alternativetitle
      } else {
        this.title = 'This Book Talks about conditionals'
      }

    }
  }

}
</script>

<style>
  .below-content {
    display: flex;
    flex-direction: column;
    justify-content: space-between;
  }
</style>
