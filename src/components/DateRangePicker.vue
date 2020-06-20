<template>
  <div class="container">
    <label class="label" for="from">From</label>
    <div class="container-inline">
      <select name="from-month" id="dp-from-month">
        <option :value="null">Pick a month</option>
      </select>
      <select name="from-year" id="dp-from-year">
        <option :value="null">Pick a year</option>
      </select>
    </div>
    <label class="label" for="to">To</label>
    <div class="container-inline">
      <select name="to-month" id="dp-to-month">
        <option :value="null">Pick a month</option>
      </select>
      <select name="to-year" id="dp-to-year">
        <option :value="null">Pick a year</option>
      </select>
    </div>
  </div>
</template>

<script>
export default {
  name: "DateRangePicker"
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
