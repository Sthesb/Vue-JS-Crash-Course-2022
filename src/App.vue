<template>
  <h2>{{ title }}</h2>
  <button @click="toggleModol" v-show="!showModol">toggle modol</button>
  <div class="" v-if="showModol">
    <Modal :header="header" content="20% off Get it now." @close="toggleModol" theme="sale"/>
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
