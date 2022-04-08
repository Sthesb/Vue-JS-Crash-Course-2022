<template>
  <h2>{{ title }}</h2>
  <!-- <button @click="toggleModol" v-show="!showModol">toggle modol</button> -->
  <teleport to=".modals" v-if="showModol">
    <Modal  @close="toggleModol" theme="" >
      <template v-slot:links>
        <a href="#">20% off</a>
      </template>
      <h1>Ninja Giveaway</h1>
      <p>hey ninja get your goodies while stock lasts</p>
    </Modal>
  </teleport>
  
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
      showModol: true
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
