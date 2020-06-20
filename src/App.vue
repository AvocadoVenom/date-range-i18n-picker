<template>
  <div id="app">
    <select id="languages" name="languages" v-model="currentLanguage">
      <option value="fr">Français</option>
      <option value="en">English</option>
    </select>
    <DateRangePicker :lang="currentLanguage" />
  </div>
</template>

<script>
import DateRangePicker from './components/DateRangePicker.vue';

export default {
  name: 'App',
  components: { DateRangePicker },
  data: () => ({ currentLanguage: 'fr' }),
};
</script>

<style lang="scss">
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  text-align: center;
  color: #2c3e50;
  margin: 60px 30% 0 30%;
}
</style>
