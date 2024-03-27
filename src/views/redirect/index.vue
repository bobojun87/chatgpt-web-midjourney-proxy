<script setup lang="ts">
import { useRoute } from 'vue-router';
const route = useRoute()
const keys = Object.keys(route.query)
const query = route.query
</script>

<template>
  <div class="home">
    <div class="title">
      跳转页面
    </div>

    <div class="content">
      <div v-for="(item, index) in keys" :key="index">
        {{ item }}: {{ query[item] }}
      </div>
    </div>
  </div>
</template>

<style lang="less" scoped>
.home {
  height: 100%;
  padding: 20px;
  background-color: #fff;

  .title {
    font-size: 30px;
    font-weight: bold;
  }

  .content {
    margin-top: 20px;
    font-size: 20px;
  }
}
</style>
