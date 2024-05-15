<template>
  <div style="height: 100vh; overflow: hidden;">
    <div class="top-blue"></div>
    <div class="banner"><img src="@/assets/img/choose.png" alt=""></div>
    <div class="bottom-green">
      <p @click="router.push({path: '/login'})">登录</p>
      <p @click="router.push({path: '/register'})">注册</p>
      <p style="border: none;">帮助</p>
    </div>
  </div>
</template>

<script setup lang="ts">
import { useRouter } from "vue-router";
const router = useRouter();

</script>

<style lang="less" scoped>
  .top-blue {
    background-color: #7B7DF0;
  }
  .banner, .content {
    img {
      width: 100%;
      display: block;
    }
  }
  .bottom-green {
    background-color: #66DBAA;
    height: 60%;
    margin-top: -1px;
    text-align: center;
    color: white;
    font-size: 16px;
    padding: 0 35%;
    p {
      border-bottom: 1px solid #fff;
      padding: 20px 0;
    }
  }
</style>