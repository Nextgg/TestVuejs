<script >
import Chart from "chart.js/auto";

const labels =[
    'jun',
    'feb',
    'march',
    'may',
    'june'
];

const data = {
  labels:labels,
  datasets:[{
    label:'Blance',
    backgroundColor:'rgb(222)',
    borderColor:'rgb(255,99,135)',
    data:[0,1,2,3,4,5,6]
  }]
}

const config = {
  type: 'line',
  data:data,
  options:{}
}
const myChart = new Chart(
    document.getElementById('myChart'),
    config
);
</script>

<template>
  <div>
    <canvas id="myChart"></canvas>
  </div>
</template>

<style scoped>

</style>