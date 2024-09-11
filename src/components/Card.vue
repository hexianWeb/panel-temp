<template>
  <div
    class="flex-1 my-4 border border-gray-300 border-opacity-50"
    style="background-color: rgba(255, 255, 255, 0.01)"
  >
    <div class="h-1/6 flex items-center justify-start p-3">
      <div
        class="title-bg-custom-image bg-top w-full bg-no-repeat bg-cover relative flex items-center"
      >
        <img src="/star.png" alt="icon" class="w-6 h-7 mr-2" />
        <span
          class="text-white text-l font-bold absolute bottom-0 left-0 mb-1 ml-6"
        >
          {{ props.titleCn }}
          <small class="font-light mb-0">{{ props.titleEn }}</small></span
        >
      </div>
    </div>
    <div class="h-4/5 p-4">
      <!-- 这里放置不同种类的Ecahrt图表 -->
      <slot></slot>
    </div>
  </div>
</template>

<script setup lang="ts">
const props = withDefaults(
  defineProps<{
    titleCn?: string;
    titleEn?: string;
  }>(),
  {
    titleCn: "生產",
    titleEn: "Manufacture",
  }
);
</script>

<style scoped>
.title-bg-custom-image {
  background-image: url("/title-bg.png");
  height: 72%;
}
</style>
