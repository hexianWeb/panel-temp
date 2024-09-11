<template>
  <div id="app" class="h-screen w-screen overflow-hidden">
    <div class="clear-both h-full">
      <!-- 中间区域 -->
      <div
        class="float-left w-full h-full bg-cover bg-top middle-bg-custom-image"
      >
        <div class="h-full" style="margin: 0 20%">
          <div class="h-full w-full">
            <Header>
              <div class="container mx-auto text-center">
                <h1 class="text-3xl font-bold text-cyan-400 m-2">
                  組 装 數 字 化 車 間
                </h1>
                <p class="text-sm text-cyan-300 m-0">
                  Assembly Digital Workshop
                </p>
              </div>
            </Header>
            <Main class="h-full relative">
              <div class="container mx-auto h-1/5 w-3/4 flex justify-between">
                <div class="flex-1 bg-red-200 h-full m-12"></div>
                <div class="flex-1 bg-red-200 h-full m-12"></div>
                <div class="flex-1 bg-red-200 h-full m-12"></div>
              </div>
              <!--底部 footer 部分  -->
              <div
                class="container mx-auto h-1/5 w-5/6 absolute bottom-40 left-0 right-0 mx-auto"
              >
                <Notification />
              </div>
            </Main>
          </div>
        </div>
      </div>

      <!-- 左侧栏 -->
      <div class="float-left w-1/5 h-full" style="margin-left: -99%">
        <div class="h-16 bg-gray-200">
          <!-- 64px高的顶部div -->
        </div>
        <div class="h-[calc(100%-64px)] flex flex-col">
          <Card title-cn="戰情" title-en="War Situation" />
          <Card />
          <Card title-cn="品質" title-en="Quality" />
        </div>
      </div>

      <!-- 右侧栏 -->
      <div class="float-left w-1/5 h-full" style="margin-left: -21%">
        <div class="h-16 bg-gray-200">
          <!-- 64px高的顶部div -->
        </div>
        <div class="h-[calc(100%-64px)] flex flex-col">
          <Card title-cn="人力" title-en="Human Resources" />
          <Card title-cn="設備" title-en="Equipment" />
          <Card title-cn="監控" title-en="Monitoring" />
        </div>
      </div>
    </div>
  </div>
</template>

<script setup lang="ts">
import Card from "./components/Card.vue";
import Notification from "./components/Notification.vue";
</script>

<style scoped>
.middle-bg-custom-image {
  background-image: url("/bg.png");
}
.title-bg-custom-image {
  background-image: url("/title-bg.png");
  height: 72%;
}
.float-left {
  float: left;
}
.relative::after {
  content: "";
  display: table;
  clear: both;
}
</style>
