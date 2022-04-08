<template>
    
    <h2>Ninja Reaction Timer</h2> <br>
    <button class="btn btn-primary" @click="start" :disabled="isPlaying">Play</button>
    <Block v-if="isPlaying" :delay="delay"  />
    <Results />
  
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

    }
  },
  methods: {
    start () {
      this.delay = 2000 + Math.random() * 50000
      this.isPlaying = true
      

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
