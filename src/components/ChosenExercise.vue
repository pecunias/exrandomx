<template>
  <div>
    <button v-on:click="getRandomExercise(exercises)"></button>
    <span>{{chosenExercise.name}}</span>
  </div>
</template>

<script>
export default {
  name: 'ChosenExercise',
  props: {
    exercises: Array 
  },
  data: function() {
    return {
      chosenExercise: {}
    }
  },
  methods: {
    getRandomExercise: function (exercises) {
      const randomIndex = Math.floor(Math.random() * exercises.length);
      this.chosenExercise = exercises[randomIndex]
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>

</style>

