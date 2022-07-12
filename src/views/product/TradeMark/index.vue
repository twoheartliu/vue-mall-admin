<template>
  <div>
    <el-button
      type="primary"
      icon="el-icon-plus"
      style="margin: 10px 0 20px"
    >添加</el-button>
    <el-table :data="tableData" style="width: 100%" border>
      <el-table-column prop="date" label="序号" width="100" align="center" />
      <el-table-column prop="name" label="品牌名称" />
      <el-table-column prop="品牌logo" label="地址" />
      <el-table-column prop="品" label="操作" />
    </el-table>
    <!--
      @size-change="handleSizeChange"
      @current-change="handleCurrentChange"
     -->
    <el-pagination
      :current-page="1"
      :page-sizes="[10, 20, 50]"
      :page-size="10"
      layout="prev, pager, next, jumper, ->, sizes, total"
      :total="99"
      style="margin-top: 20px; textalign: center"
    />
  </div>
</template>

<script>
export default {
  data() {
    return {
      tableData: [{
        date: '1',
        name: '王小虎',
        address: '上海市普陀区金沙江路 1518 弄'
      }, {
        date: '2',
        name: '王小虎',
        address: '上海市普陀区金沙江路 1517 弄'
      }, {
        date: '3',
        name: '王小虎',
        address: '上海市普陀区金沙江路 1519 弄'
      }, {
        date: '4',
        name: '王小虎',
        address: '上海市普陀区金沙江路 1516 弄'
      }]
    }
  },
  mounted() {
    console.log(this.$API)
  }
}
</script>

<style>
</style>
