<template>
  <div class="projects">
    <h1>我的项目</h1>
    <el-row :gutter="20">
      <el-col
        v-for="project in projects"
        :key="project.id"
        :xs="24"
        :sm="12"
        :md="8"
      >
        <el-card class="project-card">
          <img :src="project.image" class="project-image" />
          <h3>{{ project.title }}</h3>
          <p>{{ project.description }}</p>
          <div class="tags">
            <el-tag
              v-for="tag in project.tags"
              :key="tag"
              size="small"
              class="tag"
            >
              {{ tag }}
            </el-tag>
          </div>
          <el-button
            type="primary"
            @click="viewProject(project)"
            class="view-btn"
          >
            查看详情
          </el-button>
        </el-card>
      </el-col>
    </el-row>
  </div>
</template>

<script setup>
import { ref } from "vue";

const projects = ref([
  {
    id: 1,
    title: "电商平台",
    description: "基于Vue3和Element Plus的现代电商平台",
    image: "https://via.placeholder.com/300x200",
    tags: ["Vue3", "Element Plus", "Vite"],
  },
  {
    id: 2,
    title: "社交媒体应用",
    description: "使用Vue和Firebase构建的社交媒体应用",
    image: "https://via.placeholder.com/300x200",
    tags: ["Vue", "Firebase", "Tailwind CSS"],
  },
  {
    id: 3,
    title: "任务管理系统",
    description: "企业级任务管理系统，支持团队协作",
    image: "https://via.placeholder.com/300x200",
    tags: ["Vue", "Node.js", "MongoDB"],
  },
]);

const viewProject = (project) => {
  // 这里可以添加查看项目详情的逻辑
  console.log("查看项目：", project.title);
};
</script>

<style scoped>
.projects {
  max-width: 1200px;
  margin: 0 auto;
  padding: 2rem;
}

h1 {
  text-align: center;
  margin-bottom: 2rem;
}

.project-card {
  margin-bottom: 2rem;
  transition: transform 0.3s;
}

.project-card:hover {
  transform: translateY(-5px);
}

.project-image {
  width: 100%;
  height: 200px;
  object-fit: cover;
  border-radius: 4px;
  margin-bottom: 1rem;
}

.tags {
  margin: 1rem 0;
}

.tag {
  margin-right: 0.5rem;
  margin-bottom: 0.5rem;
}

.view-btn {
  width: 100%;
  margin-top: 1rem;
}
</style> 