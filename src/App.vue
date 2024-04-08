<script setup>
import { RouterView } from 'vue-router'
import {
  Sunny,
  MostlyCloudy,
  MoonNight
} from '@element-plus/icons-vue'
import { useRoute } from 'vue-router';
const route = useRoute();

const getActiveMenuItem = (routePath) => {
  if (routePath === '/') {
    return '1';
  } else if (routePath === '/project') {
    return '2';
  } else if (routePath === '/about') {
    return '3';
  }
};
</script>

<template>
  <el-affix :offset="0">
    <el-header>
      <div></div>
      <el-menu :default-active="getActiveMenuItem($route.path) " class="el-menu" mode="horizontal" :ellipsis="false"
        text-color="#666666" active-text-color="#6DAFE3">
        <el-menu-item index="1">
          <RouterLink to="/" class="link">
            <el-icon>
              <Sunny />
            </el-icon>
            Home
          </RouterLink>
        </el-menu-item>
        <el-menu-item index="2">
          <RouterLink to="/project" class="link">
            <el-icon>
              <MostlyCloudy />
            </el-icon>
            Projects
          </RouterLink>
        </el-menu-item>
        <el-menu-item index="3">
          <RouterLink to="/about" class="link">
            <el-icon>
              <MoonNight />
            </el-icon>
            About
          </RouterLink>
        </el-menu-item>
      </el-menu>
    </el-header>
  </el-affix>
  <router-view />
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
      font-size: 14px;
      font-family: Lucida Handwriting;
    }
  }
}
</style>
