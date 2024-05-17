<template>
    <div>
      <grand-child-component @sendData="receiveDataFromGrandChild" />
    </div>
  </template>
  
  <script>
  import GrandChildComponent from './GrandChildComponent.vue';
  
  export default {
    name: 'ChildComponent',
    components: {
      GrandChildComponent
    },
    emits: ['sendDataToParent'],
    methods: {
      receiveDataFromGrandChild(data) {
        this.$emit('sendDataToParent', data);
      }
    }
  }
  </script>
  