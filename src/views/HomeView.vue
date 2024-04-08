<script setup>
</script>

<template>
  <div class="layout">
    <el-container>
      <el-main>
        <div class="name">
          lnitia's world
          <div class="desc">no rain, no flowers</div>
        </div>
        <div class="projectcard">
          <a class="link" href="/#/project">
            <el-card shadow="hover">
              <h3>React项目</h3>动力学仿真前后处理系统
            </el-card>
          </a>
          <a class="link" href="/#/project?scrollTo=project2">
            <el-card shadow="hover">
              <h3>Vue项目</h3>研究生小组周报系统
            </el-card>
          </a>
          <a class="link" href="/#/project?scrollTo=project3">
          <el-card shadow="hover">
            <h3>HoloLens项目</h3>有限元仿真可视化系统
          </el-card>
          </a>
          <a class="link" href="http://xlinwork.online:8001" target="_blank">
            <el-card shadow="hover">
              <h3>个人知识库&博客</h3>
            </el-card>
          </a>
        </div>
        <!-- <RouterView /> -->
      </el-main>
      <el-footer>
        <p>Copyright © 2024 lnitia</p> <!-- | 微信: lnitia_90398 | 邮箱: xinlnitia@163.com -->
        <el-link class=" link" href="https://beian.mps.gov.cn/#/query/webSearch" target="_blank"
          :underline="false">川公网安备51010602002074号</el-link>
        <el-link class="link" href="https://beian.miit.gov.cn/" target="_blank"
          :underline="false">蜀ICP备2023037581号-1</el-link>
      </el-footer>
    </el-container>
  </div>
</template>

<style scoped>
.el-main {
  width: 100%;
  margin: 0;
  padding: 0;
  background: url('@/assets/bizhi.jpg') no-repeat top / cover;
  background-attachment: fixed;
  
  .name {
    font-size: 60px;
    font-family: Lucida Handwriting;
    font-weight: bold;
    color: #fff;
    text-align: center;
    padding-top: 9%;
  
    .desc {
      font-size: 30px;
      font-weight: normal;
    }
  }

  .name:hover {
      cursor: default;
  }
  
  .projectcard {
    margin-top: 200px;
    margin-bottom: 150px;
    display: flex;
    justify-content: center;

    .el-card {
      width: 220px;
      height: 100px;
      margin-right: 40px;
      border: 0;
      display: flex;
      align-items: center;
      justify-content: center;
      text-align: center;
      background-color: rgba(38, 76, 120, 0.7);
      color: #fff;
    }

    .el-card:hover {
      transform: scale(1.06);
    }
  }
}
.el-footer {
  height: 8ch;
  background-color: #0E0D0F;
  display: flex;
  align-items: center;
  justify-content: center;
  font-size: 14px;
  color: gray;
  .el-link {
    margin-left:16px;
    font-size: 14px;
    color: gray;
    &:hover {
      color: rgb(93, 93, 93);
    }
  }
}
</style>
