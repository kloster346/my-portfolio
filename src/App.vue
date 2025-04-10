<template>
  <el-container class="layout-container">
    <el-header>
      <nav>
        <router-link to="/">首页</router-link> |
        <router-link to="/projects">项目</router-link> |
        <router-link to="/about">关于我</router-link>
      </nav>
    </el-header>
    <el-main>
      <router-view />
    </el-main>
    <el-footer>
      <p>&copy; 2024 我的作品集</p>
    </el-footer>
  </el-container>
</template>

<style scoped>
.layout-container {
  min-height: 100vh;
}

.el-header {
  background-color: #fff;
  box-shadow: 0 2px 4px rgba(0, 0, 0, 0.1);
  display: flex;
  align-items: center;
  justify-content: center;
}

nav {
  padding: 1rem;
}

nav a {
  color: #333;
  text-decoration: none;
  padding: 0 1rem;
}

nav a.router-link-active {
  color: #409eff;
}

.el-main {
  padding: 2rem;
}

.el-footer {
  text-align: center;
  color: #666;
  padding: 1rem;
}
</style> 