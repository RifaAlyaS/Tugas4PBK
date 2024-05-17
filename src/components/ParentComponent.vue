<template>
    <div>
      <child-component @sendDataToParent="displayData" />
      <p>{{ receivedData }}</p>
    </div>
  </template>
  
  <script>
  import ChildComponent from './ChildComponent.vue';
  
  export default {
    name: 'ParentComponent',
    components: {
      ChildComponent
    },
    data() {
      return {
        receivedData: ''
      }
    },
    methods: {
      displayData(data) {
        this.receivedData = data;
      }
    }
  }
  </script>
  