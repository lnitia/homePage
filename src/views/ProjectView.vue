<script setup>
import {ref, onMounted} from 'vue';

const imgList1 = ref([
  { id: 0, view: 'QD1.png' },
  { id: 1, view: 'QD2.png' },
  { id: 2, view: 'QD3.png' }
])

const scrollToProject = () => {
  const search = window.location.hash.split("?")[1];
  const urlParams = new URLSearchParams(search);
  const scrollTo = urlParams.get('scrollTo');

  if (scrollTo === 'project2' || scrollTo ==='project3') {
    const project = document.getElementById(scrollTo);
    if (project) {
      project.scrollIntoView({ behavior: 'smooth' });
    }
  }
};

onMounted(() => {
  scrollToProject();
});
</script>

<template>
  <div class="projects">
    <div id="project1" class="project" style="background: linear-gradient(50deg, #97c2ea 0%, #52758f 100%)">
      <div class="projectinfo">
        <div class="title">铁道动力学仿真前后处理系统</div>
        <h3>技术栈：React + Umi + Antd pro + Fabric + Threejs + Websocket</h3>
        <div class="intro">
          • 前处理模块：仿真初始参数输入、配置文件的导入导出、二维轨道横纵可视化、三维车辆可视化<br />
          • 后处理模块：基于unity render streaming的视频流云渲染、视频界面的人机交互、结果文件导出<br />
        </div>
        <a href="http://xlinwork.online:8001/projects/01qd.html">
        <el-button round>MORE</el-button></a>
        <!-- <a href="#project2">👇</a> -->
      </div>
      <div class="projectimg">
        <img src="@/assets/QD.png" alt="" />
      </div>
    </div>
    <div id="project2" class="project" style="background: linear-gradient(-50deg, #c0c0c0 0%, #a09f9f 100%)">
      <div class="projectimg">
        <img src="@/assets/227.png" alt="" />
      </div>
      <div class="projectinfo">
        <div class="title">基于混合现实的产品设计方案可视化验证系统</div>
        <h3>技术栈：Unity + HoloLens 2 + MixedRealityToolKit</h3>
        <div class="intro">
          • 仿真结果可视化模块：有限元仿真结果映射、混合现实设备人机交互、虚实融合可视化<br />
          • 虚拟装配模块：模型干涉检测、虚拟物体实景放置、装配结果反馈<br />
        </div>
        <!-- <el-button round>MORE</el-button> -->
      </div>
    </div>
    <div id="project3" class="project" style="background: linear-gradient(50deg, #9daa86 0%, #626a54 100%)">
      <div class="projectinfo">
        <div class="title">研究生小组周报系统</div>
        <div class="intro">
          • 周报前台页面基于 Vue2 + ElementUI + mavonEditor + axios 开发<br />
          • 周报后台管理系统选用 Vue-admin-template 中后台框架，基于 Vue2 + elementUI + mavonEditor + axios + vueX 开发<br />
          • 周报后端基于 node.js，采用 express + mysql 开发，使用 joi 设置验证规则，cors 解决跨域，express-jwt 解析token等<br />
        </div>
        <!-- <el-button round>MORE</el-button> -->
      </div>
      <div class="projectimg">
        <img src="@/assets/week.png" alt="" />
      </div>
    </div>
    <div id="project4" class="project" style="background: linear-gradient(-140deg, #b0c4de 0%, #6e7c8e 100%)">
      <div class="projectimg">
        <img src="@/assets/blog.png" alt="" />
      </div>
      <div class="projectinfo">
        <div class="title">个人知识库&博客</div>
        <h3>基于VuePress静态网站生成器</h3>
        <div class="intro">
          研究生期间学习记录<br />
          • 前端三大件：HTML、CSS、JS<br />
          • 框架：Vue、React<br />
          • 混合现实开发：hololens 2、Unity、C#<br />
        </div>
        <a class="link-P" href="http://xlinwork.online:8001" target="_blank">
          <el-button round>GO TO</el-button>
        </a>
      </div>
    </div>
    <!-- <div class="projectinfo">
      <ProjectCard>
        <template #heading>铁道动力学仿真前后处理系统</template>
        <template #intro>
          <b>主要内容:</b> <br />
          该系统开发用于铁路领域动力学仿真的前处理模块和后处理模块<br />
          前处理模块：仿真初始参数输入、配置文件的导入导出、二维轨道横纵可视化、三维车辆可视化<br />
          后处理模块：基于unity render streaming的视频流云渲染、视频界面的人机交互、结果文件导出<br />
          作用：该项目所开发的系统用于为国产化动力学仿真软件提供可视化界面<br /><br />
          <b>技术栈</b>: <br />
          React: 基础框架；Umi：提供多终端自适应以及全局管理等；Antd+Antd pro: UI元素设计；Fabric: 2D
          轨道线路横纵断面预览图；Three：3D模型展示；Websocket：视频流接收<br />
          主要功能包括：仿真数据输入与校验，配置文件导出与导入，项目与用户管理， 2D轨道图形渲染，3D结果模型渲染，后处理云渲染技术，
          结果文件下载，以及与后端、unity端的交互。这使得用户无需安装专业软件，通过电脑、手机、平板网页访问，即可随时随地设置仿真<br />
          <a class="link" href="http://162.14.65.241/hyw/project/QD/qd.html" target="_blank">系统详情介绍</a>
        </template>
        <template #img>
          <img src="@/assets/QD.png" alt="" />
        </template>
      </ProjectCard>
      <ProjectCard>
        <template #heading>基于混合现实的有限元仿真结果可视化系统</template>
        <template #intro>
          <b>主要内容:</b> <br />
          该系统开发用于铁路领域有限元仿真的结果后处理模块<br />
          仿真结果可视化模块：有限元仿真结果映射、与混合现实设备的人机交互、虚实融合的可视化<br />
          虚拟装配模块：模型干涉检测、虚拟物体实景放置、装配结果反馈<br />
          作用：该项目所开发的系统用于开发国产化动力学仿真软件提供可视化界面<br /><br />
          <b>技术栈</b>: <br />
          Unity: 三维引擎；hololens2: 混合现实设备；MixedRealityToolKit: 混合现实应用开发框架<br />
          主要功能包括：有限元仿真结果(结构强度、疲劳寿命预测、静应力变形)三维可视化，可视化模型管理，通过扫描二维码实现虚拟物体与真实物体对齐融合，
          模型零部件替换后检测是否发生干涉，通过深度传感器扫描现实环境返回的网格数据实现虚拟模型在真实桌面上的放置，以及与虚拟模型、二维面板的手势交互<br />
          <a class="link" href="http://162.14.65.241/hyw/project/QD/qd.html" target="_blank">系统详情介绍</a>
        </template>
        <template #img>
          <img src="@/assets/227.png" alt="" />
        </template>
      </ProjectCard>
      <ProjectCard>
        <template #heading>研究生小组周报系统</template>
        <template #intro>
          <b>主要内容:</b> <br />
          该系统开发用于研究生小组每周组会汇报使用<br />
          周报前台：提交当周周报、展示个人所有周报、各周所有周报<br />
          周报后台：增加修改、删除周报功能、草稿箱功能、用户管理功能<br />
          后端：实现周报内容、用户信息、照片、文件增删改查功能<br />
          作用：该系统用于研究生小组汇报，可有效提高组会探讨效率<br /><br />
          <b>技术栈</b>: <br />
          周报前台页面基于Vue2 + ElementUI + mavonEditor + axios开发<br />
          周报后台管理系统选用Vue-admin-template中后台框架，基于Vue2 + elementUI + mavonEditor + axios + vueX开发<br />
          周报后端基于node.js，采用express + mysql开发，使用joi设置验证规则，cors解决跨域，express-jwt解析token等<br />
          <a class="link" href="http://162.14.65.241/hyw/project/QD/qd.html" target="_blank">系统详情介绍</a>
          <div className="enter">
            <a href="http://162.14.65.241/hyw-blog" target="_blank">
              周报前台-点击进入
            </a>
          </div>
        </template>
        <template #img>
          <img src="@/assets/227.png" alt="" />
        </template>
      </ProjectCard>
      <ProjectCard>
        <template #heading><a class="link" href="http://xlinwork.online:8001" target="_blank">知识库Blog</a></template>
        <template #intro>
          <b>主要内容:</b> <br />
          研究生期间学习记录<br />
          前端三大件：HTML、CSS、JS<br />
          框架：Vue、React<br />
          混合现实开发：hololens 2、Unity、C#<br /><br />
          <b>技术栈</b>: <br />
          基于vuePress静态网站生成器。以 md为中心的项目结构，以最少的配置帮助你专注于写作。
          享受 vue + webpack的开发体验，可以在 md 中使用 vue 组件，又可以使用 vue来开发自定义主题<br />
          vuePress 会为每个页面预渲染生成静态的html，同时，每个页面被加载的时候，将作为 spa 运行。
          内容的更新通过传入md格式文件进行，以静态页面形式部署即可<br />
        </template>
        <template #img>
          <img src="@/assets/blog.png" alt="" />
        </template>
      </ProjectCard>
    </div> -->
  </div>
</template>

<style>
.projects {
  width: 100%;

  .project{
    width: 100%;
    height:778px;
    display: flex;
    justify-content: center;
    align-items: center;

    .projectinfo {
      max-width: 650px;
      color: #fff;
      margin: 0 50px;

      .title {
        font-size: 50px;
        margin-bottom: 20px;
      }
      .intro {
        margin: 40px 0;
        line-height: 1.5;
      }
      .el-button {
        width: 100px;
        margin-left: 20px;
        border: 2px solid;
        scale: 1.3;
        color: #fff;
        background-color: transparent;
      }
    }

    .link-p {
      color: #fff; 
    }
  }
}

img {
  display: block;
  max-width: 600px;
}

#project2 {
  padding-top: 60px;    
  padding-bottom: 60px;    
  margin-bottom: -60px;
}
#project3 {
  padding-top: 60px;    
  margin-top: -60px;
}
</style>