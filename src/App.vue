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
      this.$http.get('https://translate.yandex.net/api/v1.5/tr.json/translate?key=trnsl.1.1.20171005T154827Z.1326a8a69fa352c8.fa9d303a5021deebb6ec8b42b83591aa4fce1eb0&lang=ru&text=' + text).then((response) => {
        alert(response.body.text[0]);
      })
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
