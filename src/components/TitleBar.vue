<template>
<div class="bar">
  <el-page-header :icon="null" title="XLogs">
    <template #content>
      <div class="flex items-center">
<!--        <span class="text-large font-600 mr-3"> XLogs </span>-->
        <span class="sub-title" style="color: var(--el-text-color-regular)">
          日志订阅工具
        </span>
      </div>
    </template>
  </el-page-header>
</div>
</template>
<script setup lang="ts">
</script>

<style scoped>
.bar {
  margin-top: 20px;
  margin-bottom: 25px;
  padding-left: 30px;
  padding-right: 30px;
}

.sub-title {
  font-size: 14px;
}
</style>