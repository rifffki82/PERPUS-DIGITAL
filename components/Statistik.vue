<template>
<div>
  <canvas id="statistik"></canvas>
</div>
</template>

<script setup>
import Chart from 'chart.js/auto'

const labels = [
  'january',
  'february',
  'march',
  'april',
  'mei',
  'june',
];
const data ={
  labels:labels,
  datasets:[{
    label: 'pengunjung',
    data: [6, 8,10, 7, 7,10],
    backgroundColor:[
      'rgb(255, 0, 0)',
      'rgb(255, 255, 0)',
      'rgb( 0, 255, 0)',
      'rgb(255, 69, 0)',
      'rgb(255, 69, 0)',
      'rgb( 0, 255, 0)'
    ],
  }]
};
const  config ={
  type: 'bar',
  data: data,
  options: {}
};
onMounted(()=>{
  const myChart = new Chart(
    document.getElementById('statistik'),
    config
  );
})

</script>