<template>
  <div class="dashboard-editor-container">
    <panel-group :iconClass="edit" :className="cardEditIcon" :data="data"/>
    <panel-group :data="data"/>
    <el-row style="background:#fff;padding:16px 16px 0;margin-bottom:32px;">
      <line-chart :chart-data="lineChartData" />
    </el-row>
  </div>
</template>

<script>
import PanelGroup from './components/PanelGroup'
import LineChart from './components/LineChart'
const lineChartData = {
  newVisitis:[0, 0, 0, 1, 1, 1, 0],
}
const data = {
  lists:[
    {
      text:'今日新业务',
      num:2
    },
    {
      text:'今日新业务',
      num:2
    },
    {
      text:'今日新业务',
      num:2
    },
    {
      text:'今日新业务',
      num:2
    },
  ]
} 
export default {
  name: 'DashboardAdmin',
  components: {
    PanelGroup,
    LineChart
  },
  data() {
    return {
      edit:'edit',
      cardEditIcon:'card-edit-icon',
      data:data.lists,
      lineChartData: lineChartData.newVisitis
    }
  },
  methods: {
   
  }
}
</script>

<style lang="scss" scoped>
.dashboard-editor-container {
  padding: 32px;
  background-color: rgb(240, 242, 245);
  position: relative;
  .chart-wrapper {
    background: #fff;
    padding: 16px 16px 0;
    margin-bottom: 32px;
  }
}
@media (max-width:1024px) {
  .chart-wrapper {
    padding: 8px;
  }
}
</style>
