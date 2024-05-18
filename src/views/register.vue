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
        <h1>注册中心</h1>

        <div class="custom-input">
          <p>用户名：</p>
          <input type="text">
        </div>
        <div class="custom-input">
          <p>密码：</p>
          <input type="text">
        </div>
        <div class="custom-input">
          <p>重复密码：</p>
          <input type="text">
        </div>
        <div class="custom-input">
          <p>E-MAIL:</p>
          <input type="text">
        </div>
        <div class="custom-input">
          <p>QQ：</p>
          <input type="text">
        </div>
        <div class="custom-select flex">
          <div class="left">
            <p>地区：</p>
            <select name="" id="">
              <option value="北京">北京</option>
              <option value="上海">上海</option>
              <option value="深圳">深圳</option>
            </select>
          </div>
          <div class="right">
            <p>是否公开：</p>
            <select name="" id="">
              <option value="是">是</option>
              <option value="否">否</option>
            </select>
          </div>
        </div>
        <div class="custom-input">
          <p>日记首页登记语：</p>
          <input type="text">
        </div>
        <div class="custom-select flex">
          <div class="left">
            <p>姓名：</p>
            <input type="text">
          </div>
          <div class="right">
            <p>联系方式：</p>
            <input type="text">
          </div>
        </div>

        <div class="custom-btn-box flex space-between">
          <div style="flex: 1;">
            <div class="custom-btn" @click="router.push({path: '/personal-center'})">提交注册</div>
          </div>
          <div style="flex: 1; text-align: right">
            <div class="custom-btn" style="width: 100px; background: #fff; color: #999B9F; border: 1px solid #9DC1FC; display: inline-block">重置</div>
          </div>
        </div>
        <div class="bottom-banner"><img src="@/assets/img/login-banner.png" alt=""></div>
      </div>
    </div>
  </div>
</template>

<script setup lang="ts">
import {ref} from "vue"
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
        margin-top: 15px;
        p {
          margin-bottom: 3px
        }
       input {
        width: 100%;
        background-color: #EEF0F4;
        border-color: #8C8E92;
       }
      }
      .custom-select {
        margin-top: 15px;
        .left, .right {
          flex: 1;
          p {
            margin-bottom: 3px
          }
          select, input {
            width: 90%;
            height: 32px;
            border-color: #8C8E92;
            border-radius: 5px
          }
        }
        .right {
          text-align: right
        }
      }
    
      .custom-btn-box {
        margin-top: 30px;
        .custom-btn {
          text-align: center;
          color: #fff;
          background: linear-gradient(to bottom right, #8A87F9, #3530E6);
          border-radius: 50px;
          padding: 10px 0;
        }
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