<script setup>
import ProjectCard from '@/components/ProjectCard.vue';
</script>

<template>
  <div class="project">
    <div class="homeimg">
      <div class="name">
        lnitia's world
        <div class="desc">no rain, no flowers</div>
      </div>
    </div>
    <div class="content">
      <div class="title">My Projects</div>
      <ProjectCard>
        <template #heading>铁道动力学仿真前后处理系统</template>
        <template #intro>
          <b>主要内容:</b> <br/>
          该系统开发用于铁路领域动力学仿真的前处理模块和后处理模块<br/>
          前处理模块：仿真初始参数输入、配置文件的导入导出、二维轨道横纵可视化、三维车辆可视化<br/>
          后处理模块：基于unity render streaming的视频流云渲染、视频界面的人机交互、结果文件导出<br/>
          作用：该项目所开发的系统用于为国产化动力学仿真软件提供可视化界面<br/><br/>
          <b>技术栈</b>: <br/>
          React: 基础框架；Umi：提供多终端自适应以及全局管理等；Antd+Antd pro: UI元素设计；Fabric: 2D
          轨道线路横纵断面预览图；Three：3D模型展示；Websocket：视频流接收<br/>
          主要功能包括：仿真数据输入与校验，配置文件导出与导入，项目与用户管理， 2D轨道图形渲染，3D结果模型渲染，后处理云渲染技术，
          结果文件下载，以及与后端、unity端的交互。这使得用户无需安装专业软件，通过电脑、手机、平板网页访问，即可随时随地设置仿真<br/>
          <!-- <a class="link" href="http://162.14.65.241/hyw/project/QD/qd.html" target="_blank">系统详情介绍</a> -->
        </template>
        <template #img>
          <img src="@/assets/QD.png" alt=""/>
        </template>
      </ProjectCard>
      <ProjectCard>
        <template #heading>基于混合现实的有限元仿真结果可视化系统</template>
        <template #intro>
          <b>主要内容:</b> <br/>
          该系统开发用于铁路领域有限元仿真的结果后处理模块<br/>
          仿真结果可视化模块：有限元仿真结果映射、与混合现实设备的人机交互、虚实融合的可视化<br/>
          虚拟装配模块：模型干涉检测、虚拟物体实景放置、装配结果反馈<br/>
          作用：该项目所开发的系统用于开发国产化动力学仿真软件提供可视化界面<br/><br/>
          <b>技术栈</b>: <br/>
          Unity: 三维引擎；hololens2: 混合现实设备；MixedRealityToolKit: 混合现实应用开发框架<br/>
          主要功能包括：有限元仿真结果(结构强度、疲劳寿命预测、静应力变形)三维可视化，可视化模型管理，通过扫描二维码实现虚拟物体与真实物体对齐融合，
          模型零部件替换后检测是否发生干涉，通过深度传感器扫描现实环境返回的网格数据实现虚拟模型在真实桌面上的放置，以及与虚拟模型、二维面板的手势交互<br/>
          <!-- <a class="link" href="http://162.14.65.241/hyw/project/QD/qd.html" target="_blank">系统详情介绍</a> -->
        </template>
        <template #img>
          <img src="@/assets/227.png" alt=""/>
        </template>
      </ProjectCard>
      <ProjectCard>
        <template #heading><a class="link" href="http://xlinwork.online:8001" target="_blank">知识库Blog</a></template>
        <template #intro>
          <b>主要内容:</b> <br/>
          研究生期间学习记录<br/>
          前端三大件：HTML、CSS、JS<br/>
          框架：Vue、React<br/>
          混合现实开发：hololens 2、Unity、C#<br/><br/>
          <b>技术栈</b>: <br/>
          基于vuePress静态网站生成器。以 md为中心的项目结构，以最少的配置帮助你专注于写作。
          享受 vue + webpack的开发体验，可以在 md 中使用 vue 组件，又可以使用 vue来开发自定义主题<br/>
          vuePress 会为每个页面预渲染生成静态的html，同时，每个页面被加载的时候，将作为 spa 运行。
          内容的更新通过传入md格式文件进行，以静态页面形式部署即可<br/>
        </template>
        <template #img>
          <img src="@/assets/blog.png" alt=""/>
        </template>
      </ProjectCard>
    </div>
  </div>
</template>

<style>
.homeimg {
  position: relative;
  width: 100%;
  height: 90vh;
  background: url('@/assets/bizhi.jpg') no-repeat top / 100% auto;
  display: flex;
  align-items: center;
  justify-content: center;

  .name {
    font-size: 60px;
    font-family: Lucida Handwriting;
    font-weight: bold;
    color: #fff;
    text-align: center;
    position: absolute;
    top: 20%;
    left: 50%;
    transform: translate(-50%, -50%);
    
    .desc {
      font-size: 30px;
      font-weight: normal;
    }
  }
}

.content {
  margin: 0;
  padding: 0;
  position: relative;
  width: 100%;
  .title {
    height: 200px;
    padding-top: 10px;
    font-size: 60px;
    color: #1A2B47;
    font-family: Lucida Handwriting;
    display: flex;
    align-items: center;
    justify-content: center;
    background: linear-gradient(#0E0C10, #fff);
  }
}
img {
  max-width: 600px;
}
</style>