<template>
  <div class="personal-center">
    <div class="header flex space-between">
      <div class="flex">
        <img src="@/assets/img/logo.png" style="height: 20px; width: auto; vertical-align: middle;"alt=""/>
        <div class="title">数字平台</div>
      </div>
      <img src="@/assets/img/profile-picture.png" alt="">
    </div>
    <div class="container">
      <h1>个人中心</h1>
      <div class="content">
       <p><img src="@/assets/img/house.png" alt=""> 我的作品</p>
       <div class="list">
        <div class="works flex">
          <div class="left"><img src="@/assets/img/beauty.png" alt=""></div>
          <div class="right flex">
            <div class="top">
              <p>标题：xxxxx</p>
              <p>日期：xxxxx</p>
            </div>
            <div class="bottom flex space-around">
              <div class="custom-btn" @click="router.push({path: '/create'})">编辑</div>
              <div class="custom-btn" style="background-color: #676EF9;">下载</div>
            </div>
          </div>
          <img class="delete-png" src="@/assets/img/delete.png" alt="">
        </div>
       </div>
       <div class="add-box">
        <img src="@/assets/img/add.png" alt="">
        <p>创作中心</p>
       </div>
      </div>
    </div>
  </div>
</template>

<script setup lang="ts">
import { useRouter } from "vue-router";
const router = useRouter();

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
    border-radius: 10px;
    // border: 1px solid #B0DDD8;
    background-color: #fff;
    border-top: 1px solid #fff;
    h1 {
      text-align: center;
      font-size: 20px;
      margin: 10px 0;
    }
    .content {
      padding: 10px;
      border: 1px solid #B0DDD8;
      border-radius: 10px;
      p {
        font-weight: 600;
        img {
          width: 20px;
          height: auto;
          vertical-align: text-bottom;
        }
      }
      .list {
        .works {
          border: 1px solid #B3D7FD;
          padding: 10px;
          margin-top: 20px;
          position: relative;
          .left {
            flex: 1;
            img {
              width: 100%;
              display: flex;
            }
          }
          .right {
            flex: 3;
            font-size: 12px;
            padding: 0 20px;
            flex-direction: column;
            justify-content: space-between;
            .top {
              padding-top: 10px;
              p {
                font-weight: 400 !important;
              }
            } 
            .bottom {
              padding-left: 50px;
              .custom-btn {
                  background-color: #24DFA9;
                  border-radius: 3px;
                  width: 45%;
                  padding: 2px 0;
                  text-align: center;
                  color: #fff;
                }
            }
          }
          .delete-png {
            position: absolute;
            width: 20px;
            height: auto;
            top: 10px;
            right: 10px;
          }
        }
      }
      .add-box {
        margin-top: 20px;
        border: 1px solid #B3D7FD;
        text-align: center;
        color: #3A6BBA;
        padding: 40px 0;
        img {
          width: 50px;
          height: auto
        }
      }
    }
  }
</style>