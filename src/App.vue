<template>
  <div id="app">
    <!-- 显示 Vue logo -->
    <!-- <img alt="Vue logo" src="./assets/logo.png"> -->

    <!-- <el-button type="primary">测试按钮</el-button> -->

    <!-- 显示 ECharts 图表 -->
    <div>
      <ECharts :options="chartOptions" />
    </div>
  </div>
</template>

<script>
import ECharts from './components/ECharts.vue';  // 引入 ECharts 组件

export default {
  name: 'App',
  components: {
    ECharts,  // 注册 ECharts 组件
  },
  data() {
    return {
      chartOptions: {
        title: {
          text: 'ECharts 示例',
        },
        tooltip: {},
        xAxis: {
          data: ['苹果', '香蕉', '橙子'],
        },
        yAxis: {},
        series: [
          {
            type: 'bar',
            data: [5, 20, 36],
          },
        ],
      },
    };
  },
};
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
