<template>
  <div id="app">
    <calendar />;
  </div>
</template>

<script>
  import { Calendar } from 'quasar-calendar'

export default {
  data: function () {
    return {
active: false
    }
  }
}
</script>

<style scoped>
p {
  font-size: 2em;
  text-align: center;
}
</style>
