<template>
  <div id="translateForm">
    TRANSLATE FORM
    <form v-on:submit="formSubmit">
        <input type="text" v-model="textToTranslate" placeholder="Enter a word...">
        <input type="submit" value="Translate">
    </form>
  </div>
</template>

<script>

export default {
  name: 'translateForm',
  data() {
      return {
          textToTranslate: "",
      }
  },
  methods: {
      formSubmit(e) {
          this.$emit('formSubmit', this.textToTranslate);
          e.preventDefault();
      }
  }
}
</script>

<style>
#translate {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
