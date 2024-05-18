<template>
  <div>
    <div class="header flex space-between">
      <div class="flex">
        <img src="@/assets/img/logo.png" style="height: 20px; width: auto; vertical-align: middle;"alt=""/>
        <div class="title">数字平台</div>
      </div>
      <img src="@/assets/img/rr.png" alt="">
    </div>
    <div class="container">
      <div class="login-box">
        <h1>欢迎登录</h1>
        <div class="custom-input">
          <img src="@/assets/img/user.png" alt="">
          <input type="text" placeholder="请输入用户名">
        </div>
        <div class="custom-input">
          <img src="@/assets/img/pass.png" alt="">
          <input type="password" placeholder="请输入密码">
        </div>
        <div class="remember-forget flex space-between">
          <p><input type="checkbox">记住我</p>
          <p>忘记密码</p>
        </div>
        <div class="custom-btn" @click="router.push({path: '/personal-center'})">登录</div>
        <div class="bottom-banner"><img src="@/assets/img/login-banner.png" alt=""></div>
      </div>
    </div>
  </div>
</template>

<script setup lang="ts">
import { useRouter } from "vue-router";
const router = useRouter();

</script>

<style lang="less"scoped>
  .header {
    padding: 5px;
    margin: 20px 0;
    .title {
      font-weight: 600;
    }
    img {
      width: 24px;
      height: auto
    }
  }

  .container {
    padding: 10px;
    .login-box {
      background-color: #EEF0F4;
      padding: 0 20px;
      padding-top: 50px;
      border: 1px solid #B0DDD8;
      border-radius: 10px;
      h1 {
        text-align: center;
        margin-bottom: 50px;
        font-size: 20px;
        font-weight: 600
      }
      .custom-input {
        border: 1px solid #B3B5B9;
        border-radius: 20px;
        margin: 10px 0;
        img {
          width: 20px;
          height: auto;
          vertical-align: middle;
          margin-left: 5px
        }
        input {
          border: none;
          background-color: #EEF0F4
        }
      }
      .remember-forget {
        font-size: 12px !important;
        color: #8E8F93;
        margin: 20px 0;
        input {
          vertical-align: middle;
        }
      }
      .custom-btn {
        text-align: center;
        color: #fff;
        background: linear-gradient(to bottom right, #8A87F9, #3530E6);
        border-radius: 50px;
        padding: 10px 0;
      }
      .bottom-banner {
        margin-top: 20px;
        img {
          width: 100%;
        }
      }
    }
  }
</style>