<template>
  <div id="app">
    <svg viewbox="0 0 300 300" width="300" height="300" >
      <line :x1="x1" y1=100 x2=200 y2=200 stroke="black"></line>
    <circle r=50 cx=150 @click="active = !active" :class="{'active': active}"></circle>
    </svg>
    <div>
      <input type="range" v-model="x1">
    </div>

  </div>
</template>

<script>
export default {
  data: function () {
    return {
x1: 100,
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

circle {
  fill: #333;
  transition: all 0.4s cubic-bezier(.96, .04, .04, .96);
  stroke: rgb(119, 0, 255);
  storoke-width: 1px;
}
.active{
    fill: white;
    stroke-width: 50px;
}
</style>
