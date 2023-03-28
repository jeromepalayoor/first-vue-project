<template>
  <h1>{{ title }}</h1>
  <div v-if="showModal1">
    <Modal theme="" @close="toggleModal1">
      <h1>Your first Modal!</h1>
      <p>This is your very own Modal text!</p>
      <template v-slot:links>
        <a href="#">link 1</a>
        <a href="#">link 2</a>
      </template>
    </Modal>
  </div>
  <button @click="toggleModal1">Open Normal Modal</button>
  <div v-if="showModal2">
    <Modal theme="sale" @close="toggleModal2">
      <h1>Your second Modal!</h1>
      <p>This is your very own second Modal text!</p>
      <template v-slot:links>
        <a href="#">link 1</a>
        <a href="#">link 2</a>
      </template>
    </Modal>
  </div>
  <button @click="toggleModal2">Open Sale Modal</button>
</template>

<script>
import Modal from './components/Modal.vue'
export default {
  name: 'App',
  components: {
    Modal
  },
  data() {
    return {
      title: 'My first Vue app',
      showModal1: false,
      showModal2: false
    }
  },
  methods: {
    toggleModal1() {
      this.showModal1 = !this.showModal1
    },
    toggleModal2() {
      this.showModal2 = !this.showModal2
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

button {
  margin: 0 10px;
  background-color: beige;
  border: 2px solid darkgrey;
  padding: 10px;
  border-radius: 7px;
}
</style>
