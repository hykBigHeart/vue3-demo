<template>
  <div class="personal-center">
    <div class="header flex space-between">
      <div class="title">数字平台</div>
      <img src="@/assets/img/profile-picture.png" alt="">
    </div>
    <div class="container">
      <div class="title-box">
        标题：<input type="text" placeholder="请输入">
      </div>
      <div class="beauty-box">

      </div>
    </div>
  </div>
</template>

<script setup lang="ts">

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
      height: 700px;
      background: url('@/assets/img/beauty.png') no-repeat center 0px;
      background-position: center 0px;
      background-size: cover;
      text-indent: -999px;
      border-radius: 10px;
      margin-top: 10px;
    }
  }
</style>