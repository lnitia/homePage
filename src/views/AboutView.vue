<template>
  <div class="about">
    <div class="aboutme">
      <img class=avatar src="@/assets/avatar.png" />
      <h1>许篮心<br>lnitia</h1>
    </div>
    <el-timeline style="max-width: 600px">
      <el-timeline-item timestamp="基础信息" placement="top">
        <el-card>
          <p>西南交通大学硕士研究生在读</p>
          <p>base：四川成都</p>
          <p></p>
        </el-card>
      </el-timeline-item>
      <el-timeline-item timestamp="专业技能" placement="top">
        <el-card>
          <p>前端基础：HTML、CSS、JS</p>
          <p>前端框架：VUE、React</p>
          <p>后端语言：Java、C#</p>
          <p>基于unity3D的混合现实软件开发</p>
          <p>……</p>
        </el-card>
      </el-timeline-item>
      <el-timeline-item timestamp="兴趣爱好" placement="top">
        <el-card>
          <p>摄影|尤克里里|游泳|植物|手工</p>
        </el-card>
      </el-timeline-item>
      <el-timeline-item timestamp="联系方式" placement="top">
        <el-card>
          <p>Tel：18111654823</p>
          <p>Email：18111654823@163.com</p>
        </el-card>
      </el-timeline-item>
    </el-timeline>

  </div>
</template>

<style>
  .about {
    min-height: 92vh;
    display: flex;
    align-items: center;
    
    .aboutme {
      display: flex;
      align-items: center;
      margin: 0 160px 140px 300px;
      .avatar {
        max-width: 240px;
        margin: 0 20px;
      }
    }
    .el-timeline {
      scale: 1.2;
    }
  }
</style>
