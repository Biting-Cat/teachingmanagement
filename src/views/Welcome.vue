<template>
<div>
  <el-table
    :data="tableData"
    style="width: 100%"
    :row-class-name="tableRowClassName">
    <el-table-column
      prop="date"
      label="学号"
      width="180">
    </el-table-column>
    <el-table-column
      prop="name"
      label="姓名"
      width="180">
    </el-table-column>
    <el-table-column
      prop="address"
      label="班级">
    </el-table-column>
  </el-table>
  </div>
   </template>

<style>
  .el-table .warning-row {
    background: oldlace;
  }

  .el-table .success-row {
    background: #f0f9eb;
  }
</style>

<script>
export default {
  methods: {
    tableRowClassName ({ row, rowIndex }) {
      if (rowIndex === 1) {
        return 'warning-row'
      } else if (rowIndex === 3) {
        return 'success-row'
      }
      return ''
    }
  },
  data () {
    return {
      tableData: [{
        date: '202018042001',
        name: '郑浩',
        address: '计算机学院'
      }, {
        date: '202018042001',
        name: '郑浩',
        address: '计算机学院'
      }, {
        date: '202018042001',
        name: '郑浩',
        address: '计算机学院'
      }, {
        date: '202018042001',
        name: '郑浩',
        address: '计算机学院'
      }]
    }
  }
}
</script>
