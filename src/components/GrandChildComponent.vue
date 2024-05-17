<template>
    <div>
      <button @click="sendDataToParent">Click Me</button>
    </div>
  </template>
  
  <script>
  export default {
    name: 'GrandChildComponent',
    emits: ['sendData'],
    methods: {
      sendDataToParent() {
        this.$emit('sendData', 'Data from GrandChild');
      }
    }
  }
  </script>
  