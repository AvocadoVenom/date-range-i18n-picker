<template>
  <div class="container">
    <label class="label" for="from">From</label>
    <div class="container-inline">
      <select name="from-month" id="dp-from-month">
        <option :value="null">Pick a month</option>
        <option v-for="(m, i) in months" :value="i + 1" :key="i">{{
          m
        }}</option>
      </select>
      <select name="from-year" id="dp-from-year">
        <option :value="null">Pick a year</option>
        <option v-for="y in years" :key="y" :value="y">{{ y }}</option>
      </select>
    </div>
    <label class="label" for="to">To</label>
    <div class="container-inline">
      <select name="to-month" id="dp-to-month">
        <option :value="null">Pick a month</option>
        <option v-for="(m, i) in months" :value="i + 1" :key="i">{{
          m
        }}</option>
      </select>
      <select name="to-year" id="dp-to-year">
        <option :value="null">Pick a year</option>
        <option v-for="y in years" :key="y" :value="y">{{ y }}</option>
      </select>
    </div>
  </div>
</template>

<script>
import moment from 'moment';

export default {
  name: 'DateRangePicker',
  props: { lang: { type: String, required: true } },
  computed: {
    months() {
      return moment.localeData(this.lang).months();
    },
    years: () => [2020, 2019, 2018, 2017, 2016],
  },
};
</script>

<style scoped lang="scss">
.container {
  width: 100%;
  display: flex;
  align-content: stretch;
  align-items: flex-start;
  flex-direction: column;

  > * {
    margin: 0 4px;
  }
}

.container-inline {
  display: flex;
}

select {
  margin-right: 8px;
  min-width: 150px;
  padding: 4px;
  border-radius: 4px;
}

.label {
  margin: 8px 0;
}
</style>
