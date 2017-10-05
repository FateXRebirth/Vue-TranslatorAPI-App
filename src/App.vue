<template>
  <div id="app">
    <!-- <img src="./assets/logo.png">
    <router-view></router-view> -->
    <h1> Word Translator </h1>
    <h5> Powered by Vue.Js </h5>
    <TranslateForm v-on:formSubmit="translateText"></TranslateForm>

  </div>
</template>

<script>
import TranslateForm from './components/TranslateForm';


export default {
  name: 'app',
  components: {
    TranslateForm,
  },
  methods: {
    translateText(text) {
      alert(text);
    }
  }
}
</script>

<style>
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
