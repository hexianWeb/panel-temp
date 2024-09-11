<template>
  <div
    class="text-white p-4 rounded-lg w-full h-48"
    style="
      background: radial-gradient(circle, rgba(255, 0, 0, 0.37), transparent);
    "
  >
    <div class="flex h-full">
      <!-- 左侧图标 -->
      <div class="w-1/4.5 flex-shrink-0 flex items-center justify-center">
        <div class="w-50 h-50">
          <img
            src="/lab.png"
            alt="Notification icon"
            class="rounded-lg w-full h-full object-cover"
          />
        </div>
      </div>

      <!-- 右侧通知列表 -->
      <ul class="w-3.5/4.5 flex flex-col justify-between">
        <li
          v-for="(notification, index) in notifications"
          :key="index"
          class="flex items-center h-1/3"
        >
          <span class="text-red-500 mr-2 text-3xl flex-shrink-0 mr-4">•</span>
          <span class="text-base font-bold flex-grow truncate">{{
            notification.message
          }}</span>
          <span class="text-xs text-gray-400 ml-2 flex-shrink-0">{{
            notification.timestamp
          }}</span>
        </li>
      </ul>
    </div>
  </div>
</template>

<script setup>
import { ref } from "vue";

const notifications = ref([
  { message: "點膠機設備异常, 請儘快處理", timestamp: "2024-09-11 15:30:10" },
  {
    message: "點膠機設備异常, 點膠機設備异常, 请尽快处理",
    timestamp: "2024-09-11 14:11:13",
  },
  {
    message: "點膠機設備异常异常, 请尽快处理",
    timestamp: "2024-09-11 10:11:10",
  },
]);
</script>

<style scoped>
/* 自定义类来实现1:3.5的宽度比例 */
.w-1\/4\.5 {
  width: 22.22%; /* 约等于1/4.5 */
}
.w-3\.5\/4\.5 {
  width: 77.78%; /* 约等于3.5/4.5 */
}
</style>
