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
    type: '消息',
    origin: 'OA服务',
    preview: 'Los Angeles',
  },
  {
    date: '2024-05-02 18:12:11',
    type: '消息',
    origin: '系统服务',
    preview: 'Los Angeles',
  },
  {
    date: '2024-05-01 13:12:11',
    type: '警告',
    origin: '事务管理',
    preview: 'Los Angeles',
  },
  {
    date: '2024-05-01 01:12:11',
    type: '错误',
    origin: 'SRM系统',
    preview: 'Los Angeles',
  }, {
    date: '2024-05-01 01:12:11',
    type: '错误',
    origin: 'SRM系统',
    preview: 'Los Angeles',
  }, {
    date: '2024-05-01 01:12:11',
    type: '错误',
    origin: 'SRM系统',
    preview: 'Los Angeles',
  }, {
    date: '2024-05-01 01:12:11',
    type: '错误',
    origin: 'SRM系统',
    preview: 'Los Angeles',
  }, {
    date: '2024-05-01 01:12:11',
    type: '错误',
    origin: 'SRM系统',
    preview: 'Los Angeles',
  }, {
    date: '2024-05-01 01:12:11',
    type: '错误',
    origin: 'SRM系统',
    preview: 'Los Angeles',
  }, {
    date: '2024-05-01 01:12:11',
    type: '错误',
    origin: 'SRM系统',
    preview: 'Los Angeles',
  }, {
    date: '2024-05-01 01:12:11',
    type: '错误',
    origin: 'SRM系统',
    preview: 'Los Angeles',
  }, {
    date: '2024-05-01 01:12:11',
    type: '错误',
    origin: 'SRM系统',
    preview: 'Los Angeles',
  }, {
    date: '2024-05-01 01:12:11',
    type: '错误',
    origin: 'SRM系统',
    preview: 'Los Angeles',
  }, {
    date: '2024-05-01 01:12:11',
    type: '错误',
    origin: 'SRM系统',
    preview: 'Los Angeles',
  }, {
    date: '2024-05-01 01:12:11',
    type: '错误',
    origin: 'SRM系统',
    preview: 'Los Angeles',
  }, {
    date: '2024-05-01 01:12:11',
    type: '错误',
    origin: 'SRM系统',
    preview: 'Los Angeles Angeles Angeles Angeles Angeles Angeles Angeles',
  }, {
    date: '2024-05-01 01:12:11',
    type: '错误',
    origin: 'SRM系统',
    preview: 'Los Angeles',
  },
]

</script>

<template>
  <div class="table-box">
    <el-table
        :data="tableData"
        style="width: 100%; height: 100%"
        empty-text="暂无记录"
        show-overflow-tooltip
    >
      <el-table-column prop="origin" sortable label="消息来源"/>
      <el-table-column prop="type" sortable label="消息类型">
        <template #default="scope">
          <el-tag
              :type="scope.row.type === '错误' ? 'danger' : scope.row.type == '警告' ? 'warning' : 'primary'"
              disable-transitions
          >{{ scope.row.type }}
          </el-tag>
        </template>
      </el-table-column>
      <el-table-column prop="preview" label="消息概览"/>
      <el-table-column prop="date" sortable label="记录时间"/>
      <el-table-column fixed="right" label="操作">
        <template #default>
          <el-button link type="primary" size="small" @click="handleClick">
            详情
          </el-button>
          <el-button link type="primary" size="small">复制</el-button>
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