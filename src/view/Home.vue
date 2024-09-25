<template>
  <TitleBar/>
  <div class="tab_div">
    <el-tabs v-model="activeName" class="tabs" @tab-click="handleClick" tab-position="top" stretch>
      <el-tab-pane label="概览" name="first"><Message/></el-tab-pane>
      <el-tab-pane disabled label="服务" name="second">Config</el-tab-pane>
      <el-tab-pane label="订阅" name="third"><Subscription/></el-tab-pane>
      <el-tab-pane disabled label="设置" name="fourth">Task</el-tab-pane>
    </el-tabs>
  </div>
</template>

<script lang="ts" setup>
import {ref} from 'vue'
import type {TabsPaneContext} from 'element-plus'
import TitleBar from "../components/TitleBar.vue";
import Message from "./Message.vue";
import Subscription from "./Subscription.vue";

const activeName = ref('first')

const handleClick = (tab: TabsPaneContext, event: Event) => {
  console.log(tab, event)
}
</script>

<style>
.tab_div{
  margin-top: 15px;
  padding-left: 30px;
  padding-right: 30px;
  height: 100%;
}

.tabs{
  //display: block;
  height: 100%;
}
</style>