<script setup>
import {
  HomeFilled,
  Management,
  UserFilled
} from '@element-plus/icons-vue'
</script>

<template>
  <div class="layout">
      <el-container>
        <el-affix :offset="0">
          <el-header>
            <div></div>
              <el-menu
                :default-active="$route.path"
                class="el-menu"
                mode="horizontal"
                :ellipsis="false"
                @select="handleSelect"
              >
                <el-menu-item index="1"><el-icon><HomeFilled /></el-icon><RouterLink to="/" class="link">Home</RouterLink></el-menu-item>
                <el-menu-item><el-icon><Management /></el-icon><a class="link" href="http://xlinwork.online:8001" target="_blank">Blog</a></el-menu-item>
                <el-menu-item index="2"><el-icon><UserFilled /></el-icon><RouterLink to="/about" class="link">About</RouterLink></el-menu-item>
              </el-menu>
          </el-header>
        </el-affix>
        <el-main><RouterView /></el-main>
        <el-footer>
          <p>Copyright © 2024 lnitia</p> <!-- | 微信: lnitia_90398 | 邮箱: xinlnitia@163.com -->
          <el-link class="link" href="https://beian.mps.gov.cn/#/query/webSearch" target="_blank" :underline="false">川公网安备 51010602002074号</el-link>
          <el-link class="link" href="https://beian.miit.gov.cn/" target="_blank" :underline="false">蜀ICP备2023037581号-1</el-link>
        </el-footer>
      </el-container>
    </div>
</template>

<style scoped>
.el-header {
  width: 100%;
  background-color: #fff;
  display: flex;
  align-items: center;
  justify-content: center;
  .el-menu {
    border-bottom: none;
    text-decoration: none;
    background-color: rgba(0, 0, 0, 0);
    .el-menu-item {
      font-size: 17px;
    }
  }
}
.el-main {
  width: 100%;
  margin: 0;
  padding: 0;
}
.el-footer {
  height: 14ch;
  background-color: #fff;
  display: flex;
  align-items: center;
  justify-content: center;
  font-size: 18px;
  color: gray;
  .el-link {
    margin-left:16px;
    font-size: 18px;
    color: gray;
    &:hover {
      color: rgb(93, 93, 93);
    }
  }
}
</style>
