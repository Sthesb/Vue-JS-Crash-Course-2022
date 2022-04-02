<template>
  <h2>{{ title }}</h2>
  <Modal />
  
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
    }
  }
}
</script>

<style>

</style>
