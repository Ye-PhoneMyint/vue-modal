<template>
  <h1>{{title}}</h1>
  <p>Welcome...</p>
  <div v-if="showModal">
    <Modal theme="" @close="toggleModal">
      <template v-slot:links>
        <a href="">sign up now</a>
        <a href="">more info</a>
      </template>
      <h1>Sign up for the Giveway!</h1>
      <p>Grab your ninja swag for half price!</p>
    </Modal>
  </div>
  <button @click.alt="toggleModal">open modal (alt)</button>
</template>

<script>
import Modal from './components/Modal'
export default {
  components: { Modal },
  data() {
    return {
      title: "My First Vue App :)",
      showModal: false
    }
  },
  methods: {
    toggleModal() {
      this.showModal = !this.showModal
    }
  }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}

h1 {
  border-bottom: 1px solid #ddd;
  display: inline-block;
  padding: 10px;
}
</style>
