<template>
    <div ref="chart" style="width: 100%; height: 400px;"></div>
  </template>
  
  <script>
  import * as echarts from 'echarts';
  
  export default {
    name: 'ECharts',
    props: {
      options: {
        type: Object,
        required: true,
      },
    },
    mounted() {
      this.initChart();
    },
    methods: {
      initChart() {
        const chart = echarts.init(this.$refs.chart);
        chart.setOption(this.options);
      },
    },
  };
  </script>
  