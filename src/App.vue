<template>
  <div>
    <h1>{{ title }}</h1>
    <p>Welcome...</p>
    <div v-if=showModal>
    <Modal :header="header" :text="text" theme="sale" @close="toggleModal"/> 
    </div>
    <button @click="toggleModal">Open Modal</button>
  </div>
</template>

<script>

import Modal from './components/Modal'

export default {
  name: "App",
  components: {Modal},
  data() {
    return {
      title: "My first vue app",
      header: 'Sign up for the giveaway',
      text: 'Grab your ninja!!',
      showModal: false
    };
  }, 
  methods: {
    toggleModal () {
      this.showModal = !this.showModal
    }
  }
};
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
  padding-bottom: 10px;
}
</style>
