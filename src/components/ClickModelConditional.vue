
<template>
  <div class="age-increase">
    <h1 class="title-1"> All Together </h1>

    <button @click="showcontents">
      <span v-if="showcontent"> Hide content </span>
      <span v-else> Show Content </span>
    </button>


    <div class="students" v-if="showcontent">
      <h2> {{ school[0].student }} - {{ school[0].classname }} - {{ school[0].age }} <input type="text" v-model="school[0].student">  </h2>
      <h2> {{ school[1].student }} - {{ school[1].classname }} - {{ school[1].age }} <input type="text" v-model="school[1].age"></h2>
      <h2> {{ school[2].student }} - {{ school[2].classname }} - {{ school[2].age }} </h2>

      <button @click="school[0].age++"> Increase the age of first student </button>
      <button @click="school[1].age--"> Decrease the age of second student </button>

    </div>



  </div>
</template>

<script>
export default {

  data() {
    return {

      school: [
        {student: 'Mehdi',
        classname: 'B',
        age: 30
        },

        {student: 'Mike',
        classname: 'c',
        age: 20
        },

        {student: 'George',
        classname: 'D',
        age: 77
        },
      ],

      showcontent: true,

      text: ''
    }
  },

  methods: {

    showcontents() {
      this.showcontent = !this.showcontent
    }
  }

}
</script>

<style scoped>
  .title-1 {
    padding: 0;
    margin: 0;
    color: red;
    text-align: center;
  }

  .students {
    display: flex;
    flex-direction: column;
  }
</style>
