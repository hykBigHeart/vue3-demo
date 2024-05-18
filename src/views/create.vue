<template>
  <div class="personal-center">
    <div class="header flex space-between">
      <img src="@/assets/img/back.png" alt="" @click="router.back()">
      <img src="@/assets/img/profile-picture.png" alt="">
    </div>
    <div class="container">
      <div class="title-box">
        标题：<input type="text" placeholder="请输入">
      </div>
      <div class="beauty-box">
        <div class="fn-box flex">
          <div class="left">
            <select name="" id="">
              <option value="温柔女声-思琪">温柔女声-思琪</option>
              <option value="温柔女声-佩瑶">温柔女声-佩瑶</option>
              <option value="温柔女声-月月">温柔女声-月月</option>
            </select>
          </div>
          <div class="right flex">
            音量
            <input type="range" min="0" max="100" v-model="pinPadding" style="z-index: 9" />
            <span>{{ pinPadding }}</span>
          </div>
        </div>
      </div>

      <div class="bottom-box">
        <div class="btn-box flex space-around">
          <div class="custom-btn">数字</div>
          <div class="custom-btn" style="background-color: #fff; color: black">视频背景</div>
        </div>
        <div class="list flex">
          <div><img src="@/assets/img/last.png" alt=""></div>
          <div class="seize-a-seat"></div>
          <div><img src="@/assets/img/last.png" alt=""></div>
          <div class="seize-a-seat"></div>
          <div><img src="@/assets/img/last.png" alt=""></div>
        </div>
      </div>
    </div>
  </div>
</template>

<script setup lang="ts">
import { ref } from "vue"
import { useRouter } from "vue-router";
const router = useRouter();

const pinPadding = ref(0)
</script>

<style lang="less"scoped>
  .personal-center {
    background-color: #EDF1F4;
  }
  .header {
    padding: 5px;
    // margin: 20px 0;
    .title {
      font-weight: 600;
    }
    img {
      width: 24px;
      height: auto
    }
  }

  .container {
    .title-box {
      padding: 0 5px;
      input {
        width: 86%;
        border: none;
      }
    }
    .beauty-box {
      width: 100%;
      height: 600px;
      background: url('@/assets/img/beauty.png') no-repeat center 0px;
      background-position: center 0px;
      background-size: cover;
      border-radius: 10px;
      margin-top: 10px;
      padding: 10px;
      .fn-box {
        .left, .right {
          flex: 1
        }
        .left {
          select {
            width: 100%;
            height: 100%;
            outline: none;
            border-radius: 5px;
          }
        }
        .right {
          color: #fff;
          font-size: 12px;
          align-items: center;
          justify-content:  flex-end;
          input {
            width: 50%;
            margin: 0 3px;
          }
          span {
            background-color: #fff;
            color: black;
            padding: 2px 8px;
            border-radius: 3px;
          }
        }
      }
    }
    
    .bottom-box {
      border-radius: 10px;
      padding: 20px;
      background-color: #fff;
      margin-top: 10px;
      .btn-box {
        .custom-btn {
          background-color: #676EF9;
          border-radius: 20px;
          width: 45%;
          padding: 5px 0;
          text-align: center;
          color: #fff;
        }
      }
      .list {
        margin-top: 20px;
        div {
          flex: 1;
          img {
            width: 100%;
          }
        }
        .seize-a-seat {
          flex: .3;
        }
      }
    }
  }
</style>