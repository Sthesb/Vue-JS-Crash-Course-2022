<template>
    
    <h2>Ninja Reaction Timer</h2> <br>
    <button class="btn btn-primary" @click="start" :disabled="isPlaying">Play</button>
    <Block v-if="isPlaying" :delay="delay" @end="endGame" />
    <h4 v-if="score !== null">Reaction time: {{ score }} ms</h4>
    <Results v-if="score !== null" :score="score" />
  
</template>

<script>
import Block from './components/Block.vue'
import Results from './components/Results.vue'

export default {
  name: 'App',
  components: { Block, Results },
  data () {
    return {
      isPlaying: false,
      delay: null,
      score: null,
      result: ''
    }
  },
  methods: {
    start () {
      this.score = null;
      this.result = ''
      this.delay = 2000 + Math.random() * 5000
      this.isPlaying = true
    },
    endGame(reactionTimer){
      this.isPlaying = false;
      this.score = reactionTimer;

      


    }
  }
  
}
</script>

<style>

#app {
  text-align: center;
}
.app  h2 {
  color: rgb(35, 0, 68);
  text-transform: capitalize;
}


</style>
