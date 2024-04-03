<template>
  <div class="app-container">
    <el-card>
      <el-timeline style="max-width: 600px">
        <el-timeline-item v-for="item in data" :key="item.uuid" :timestamp="item.time" placement="top">
          <el-card>
            <h4>{{ item.title }}</h4>
            <p>{{ item.content }}</p>
          </el-card>
        </el-timeline-item>
      </el-timeline>
    </el-card>
  </div>
</template>

<script lang="ts" setup>
import { reactive } from "vue"
const data = reactive([
  {
    uuid: 1,
    time: "2018 / 4 / 12",
    title: "Update Github template",
    content: "Tom committed 2018/4/12 20:45"
  },
  {
    uuid: 2,
    time: "2018 / 4 / 3",
    title: "Update Github template",
    content: "Tom committed 2018/4/3 20:46"
  },
  {
    uuid: 3,
    time: "2018 / 4 / 2",
    title: "Update Github template",
    content: "Tom committed 2018/4/2 20:46"
  }
])
</script>
