<template>
<div class="container">
 <div class="block">
<el-row :gutter="10">
  <el-col :span="12">
       <el-date-picker
      v-model="value1"
      type="daterange"
      range-separator="至"
      start-placeholder="开始日期"
      end-placeholder="结束日期"
    ></el-date-picker>
  </el-col>
  <el-col :span="12"><el-button type="primary" icon="el-icon-search" class="search">搜索</el-button></el-col>
</el-row>
  </div>
  <div class="table">
<el-table
    :data="tableData"
    border
    style="width: 100%">
    <el-table-column
      prop="date"
      label="业务类型"
      width="30%">
    </el-table-column>
    <el-table-column
      prop="name"
      label="普惠"
      width="30%">
    </el-table-column>
    <el-table-column
      prop="address"
      label="30%">
    </el-table-column>
  </el-table>
  </div>
</div>
</template>
<script>
 export default {
    data() {
      return {
        value1: '',
        tableData: [{
          date: '2016-05-02',
          name: '王小虎',
          address: '上海市普陀区金沙江路 1518 弄'
        }, {
          date: '2016-05-04',
          name: '王小虎',
          address: '上海市普陀区金沙江路 1517 弄'
        }, {
          date: '2016-05-01',
          name: '王小虎',
          address: '上海市普陀区金沙江路 1519 弄'
        }, {
          date: '2016-05-03',
          name: '王小虎',
          address: '上海市普陀区金沙江路 1516 弄'
        }]
      }
    }
  }
</script>
<style lang="scss" scoped>
.container{
    padding: 0 20px 0 20px;
}
.block{
    margin: 10px 0 20px 40px;
}
.el-range-editor.el-input__inner{
    width: 100%;
}
</style>