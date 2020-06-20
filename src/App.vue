<template>
  <div id="app">
    <DateRangePicker />
  </div>
</template>

<script>
import DateRangePicker from './components/DateRangePicker.vue';

export default {
  name: 'App',
  components: { DateRangePicker },
};
</script>

<style lang="scss">
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin: 60px 30% 0 30%;
}
</style>
