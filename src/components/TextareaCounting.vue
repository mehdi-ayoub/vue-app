<template>
  <div class="age-increase">
    <h1> This is a characters counting app </h1>
    <textarea name="textarea" id="text-area" cols="" rows="10" v-model="text"></textarea>
    <div>
      <p> word count: {{ charCount }} </p>
    </div>
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

    charCount() {
      return this.text.length
    }
  }
}
</script>

<style>

</style>
