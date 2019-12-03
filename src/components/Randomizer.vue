<template>
  <div>
    <div v-for="(bodypart) in directory.bodyparts" v-bind:key="bodypart.id">
      {{bodypart.name}}
      <div v-for="(muscle) in bodypart.muscles" v-bind:key="muscle.id">
        {{muscle.name}}
        <ChosenExercise :exercises="muscle.exercises" />
      </div>
      <hr />
    </div>
</div>

</template>

<script>
import directory from '../data/directory.json'
import ChosenExercise from './ChosenExercise'
export default {
  name: 'Randomizer',
  components: {
    ChosenExercise
  },
  data: function() {
    return {
      directory,
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>

</style>

