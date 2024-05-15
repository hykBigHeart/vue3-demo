<template>
  <div class="dashboard">
    <div class="header flex space-between">
      <div class="title">数字平台</div>
      <van-button type="primary" size="mini" @click="router.push({path: '/choose'})">登录/注册</van-button>
    </div>

    <div class="banner"><img src="@/assets/img/banner.png" alt=""></div>

    <div class="video-box">
      <div id="meedu-player-container"></div>
    </div>

    <div class="big-button-box">
      <div class="big-button">
        <h4>人人都是大明星</h4>
        <p><span style="color: #069159;">100+</span>数字人形象</p>
      </div>
    </div>    

    <div class="advertisement">免拍摄/免出镜/无时间限制</div>

    <div class="content" style="padding: 0 20px;"><img src="@/assets/img/content.png" alt=""></div>

    <div class="footer">
      <h4>每个人都是自己故事的主角</h4>
      <div class="custom-btn">开始使用</div>
      <div class="custom-btn" style="background-color: #00DFA6;">联系我们</div>
      <div class="bottom-title">数字平台</div>
      <p class="website">winfun@ai.com</p>
      <p class="website">Copyright 0 winfun.ai</p>
    </div>

  </div>
</template>

<script setup lang="ts">
import { onMounted } from "vue"
import { useRouter } from "vue-router";
const router = useRouter();

  onMounted(()=> {
    new window.DPlayer({
      container: document.getElementById("meedu-player-container"),
      autoplay: true,
      video: {
        url: '',
      }
    });
  })

</script>

<style lang="less"coped>
  .header {
    padding: 5px;
    .title {
      font-weight: 600;
    }
  }
  .banner, .content {
    img {
      width: 100%;
    }
  }
  
  .video-box {
    padding: 20px;
  }

  .big-button-box {
    padding: 0 20px;
    .big-button {
      text-align: center;
      color: #fff;
      background: linear-gradient(to bottom right, #5FFFC2, #9DA5F6);
      border-radius: 50px;
      padding: 10px 0;
      line-height: 30px;
      h4 {
        font-size: 20px;
      }
    }
  }

  .advertisement {
    text-align: center;
    margin: 10px 0;
    font-size: 12px;
  }
  
  .footer {
    background-color: #262B39;
    color: #fff;
    text-align: center;
    padding: 20px 55px;
    h4 {
      font-size: 20px;
      margin-bottom: 20px;
    }
    .custom-btn {
      background-color: #9DA0FF;
      border-radius: 10px;
      padding: 10px 0;
      font-size: 18px;
      margin: 10px 0;
    }
    .bottom-title {
      font-weight: 600;
      margin-bottom: 20px;
    }
    .website {
      font-size: 12px;
      color: #FBFDFF;
      margin: 5px 0;
    }
  }


</style>