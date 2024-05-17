<template>
  <div id="app">
    <parent-component class="parent-component"/>
    <parent-with-slot-component />
  </div>
</template>

<script>
import ParentComponent from './components/ParentComponent.vue';
import ParentWithSlotComponent from './components/ParentWithSlotComponent.vue';
import './style.css'; 

export default {
  name: 'App',
  components: {
    ParentComponent,
    ParentWithSlotComponent
  }
}
</script>
