<template>
    <button v-on:click="displayAlert('Hello 👋')">{{ myText }}</button>
  </template>
  
  <script>
  export default {
    name: 'MyButton',
    props: {
      myText: String
    },
    data: function() {
      return {
      }
    },
    methods: {
      displayAlert(textToDisplay) {
        alert('message ' + textToDisplay);
      }
    }
  }
  </script>
  