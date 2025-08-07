<template>
  <button @click="showPopup = true">Show Popup</button>
  <LowTickPopup v-show="showPopup" @close="closePopup" />
</template>

<script>
import LowTickPopup from './components/Mopup.vue'


export default {
  name: 'App',
  components: {
    LowTickPopup,
  },
  data() {
    return {
      showPopup: false,
    }
  },
  methods: {
    closePopup(name) {
      this.showPopup = false
      console.log('name', name)
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
</style>
