<template>
  <h2>{{ title }}</h2>
  <button @click="toggleModol" v-show="!showModol">toggle modol</button>
  <div class="" v-if="showModol">
    <Modal  @close="toggleModol" theme="sale" >
      <template v-slot:links>
        <a href="#">20% off</a>
      </template>
      <h1>Ninja Giveaway</h1>
      <p>hey ninja get your goodies while stock lasts</p>
    </Modal>
  </div>
  
</template>

<script>
import Modal from './components/Modal/Modal.vue'

export default {
  name: 'App',
  components: {
    Modal
  },
  data () {
    return {
      title: 'Learning VueJS',
      toogle: false,
      header: "Sign up for a giveaway",
      showModol: false
    }
  },
  methods: {
    toggleModol () {
      this.showModol = !this.showModol
    }
  }
  
}
</script>

<style>

</style>
