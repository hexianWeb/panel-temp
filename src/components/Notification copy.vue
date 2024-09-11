<template>
  <div class="bg-[#1a1b26] text-white p-4 rounded-lg w-full h-full">
    <div class="flex items-start mb-2">
      <div class="w-48 w-48 mr-4 flex-shrink-0">
        <img src="/Group 55.png" alt="Notification icon" class="rounded-lg" />
      </div>
      <ul class="space-y-1 flex-grow">
        <li
          v-for="(notification, index) in notifications"
          :key="index"
          class="flex items-baseline"
        >
          <span class="text-red-500 mr-2 text-lg">•</span>
          <span class="text-sm flex-grow">{{ notification.message }}</span>
          <span class="text-xs text-gray-400 ml-2 flex-shrink-0">{{
            notification.timestamp
          }}</span>
        </li>
      </ul>
    </div>
  </div>
</template>

<script setup lang="ts">
import { ref } from "vue";

const notifications = ref([
  { message: "融资股价异常, 请尽快处理", timestamp: "2024-09-11 15:30:10" },
  {
    message: "融资股价异常, 融资股价异常, 请尽快处理",
    timestamp: "2024-09-11 14:11:13",
  },
  { message: "融资股价异常异常, 请尽快处理", timestamp: "2024-09-11 10:11:10" },
]);
</script>

<style scoped>
/* 如果需要任何额外的样式，可以在这里添加 */
</style>
