<script setup>

import {onMounted} from "vue";

const handleClick = () => {
  console.log('click')
}
onMounted(() => {

});

const tableData = [
  {
    date: '2024-05-03 01:12:11',
    type: '文件',
    origin: 'OA服务',
    preview: 'Los Angeles',
  },
  {
    date: '2024-05-02 18:12:11',
    type: '文件',
    origin: '系统服务',
    preview: 'Los Angeles',
  },
  {
    date: '2024-05-01 13:12:11',
    type: 'API',
    origin: '事务管理',
    preview: 'Los Angeles',
  },
  {
    date: '2024-05-01 01:12:11',
    type: '文件',
    origin: 'SRM系统',
    preview: 'Los Angeles',
  }, {
    date: '2024-05-01 01:12:11',
    type: '文件',
    origin: 'SRM系统',
    preview: 'Los Angeles',
  },
]

</script>

<template>
  <div class="table-box">
    <el-button icon="Odometer" type="primary" size="small" style="margin-bottom: 10px">添加订阅</el-button>
    <el-table
        :data="tableData"
        style="width: 100%; height: 100%"
        empty-text="暂无记录"
        show-overflow-tooltip
    >

      <el-table-column prop="origin" sortable label="订阅名称"/>
      <el-table-column prop="type" label="订阅方式"/>
      <el-table-column prop="date" sortable label="最近更新"/>
      <el-table-column fixed="right" label="操作">
        <template #default>
          <el-button link type="success" size="small" @click="handleClick">
            刷新
          </el-button>
          <el-button link type="primary" size="small" @click="handleClick">
            编辑
          </el-button>
          <el-button link type="danger" size="small" @click="handleClick">
            删除
          </el-button>
        </template>
      </el-table-column>
    </el-table>
  </div>

</template>

<style scoped>

.table-box {
  height: calc(100vh - 200px);
}


</style>