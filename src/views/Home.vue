<template>
  <div class="home">
    <el-row justify="center" align="middle" class="hero">
      <el-col :span="16" class="text-center">
        <h1>欢迎来到我的作品集</h1>
        <p class="subtitle">前端开发工程师 / UI设计师</p>
        <el-button
          type="primary"
          size="large"
          @click="$router.push('/projects')"
        >
          查看我的项目
        </el-button>
      </el-col>
    </el-row>

    <el-row :gutter="20" class="skills-section">
      <el-col :span="24">
        <h2>技能专长</h2>
      </el-col>
      <el-col :xs="24" :sm="8">
        <el-card>
          <template #header>
            <div class="card-header">
              <h3>前端开发</h3>
            </div>
          </template>
          <p>Vue.js, React, JavaScript, HTML5, CSS3</p>
        </el-card>
      </el-col>
      <el-col :xs="24" :sm="8">
        <el-card>
          <template #header>
            <div class="card-header">
              <h3>UI/UX设计</h3>
            </div>
          </template>
          <p>Figma, Adobe XD, 用户体验设计</p>
        </el-card>
      </el-col>
      <el-col :xs="24" :sm="8">
        <el-card>
          <template #header>
            <div class="card-header">
              <h3>其他技能</h3>
            </div>
          </template>
          <p>Git, Webpack, Node.js</p>
        </el-card>
      </el-col>
    </el-row>
  </div>
</template>

<style scoped>
.home {
  max-width: 1200px;
  margin: 0 auto;
  padding: 2rem;
}

.hero {
  min-height: 60vh;
  display: flex;
  align-items: center;
  text-align: center;
}

.hero h1 {
  font-size: 3rem;
  margin-bottom: 1rem;
}

.subtitle {
  font-size: 1.5rem;
  color: #666;
  margin-bottom: 2rem;
}

.skills-section {
  margin-top: 4rem;
}

.skills-section h2 {
  text-align: center;
  margin-bottom: 2rem;
}

.el-card {
  margin-bottom: 1rem;
  transition: transform 0.3s;
}

.el-card:hover {
  transform: translateY(-5px);
}

.card-header h3 {
  margin: 0;
  color: #409eff;
}
</style> 