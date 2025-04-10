<template>
  <div class="about">
    <el-row justify="center">
      <el-col :span="16">
        <div class="profile-section">
          <el-avatar :size="150" src="https://via.placeholder.com/150" />
          <h1>关于我</h1>
          <p class="bio">
            我是一名充满热情的前端开发工程师，专注于创建美观且用户友好的web应用。
            拥有多年的开发经验，精通现代前端技术栈。
          </p>
        </div>

        <div class="experience-section">
          <h2>工作经历</h2>
          <el-timeline>
            <el-timeline-item
              v-for="(experience, index) in experiences"
              :key="index"
              :timestamp="experience.period"
              placement="top"
            >
              <el-card>
                <h3>{{ experience.company }}</h3>
                <h4>{{ experience.position }}</h4>
                <p>{{ experience.description }}</p>
              </el-card>
            </el-timeline-item>
          </el-timeline>
        </div>

        <div class="contact-section">
          <h2>联系方式</h2>
          <el-row :gutter="20">
            <el-col :span="8">
              <el-card>
                <i class="el-icon-message"></i>
                <h3>邮箱</h3>
                <p>example@email.com</p>
              </el-card>
            </el-col>
            <el-col :span="8">
              <el-card>
                <i class="el-icon-phone"></i>
                <h3>电话</h3>
                <p>+86 123 4567 8900</p>
              </el-card>
            </el-col>
            <el-col :span="8">
              <el-card>
                <i class="el-icon-location"></i>
                <h3>地址</h3>
                <p>中国上海</p>
              </el-card>
            </el-col>
          </el-row>
        </div>
      </el-col>
    </el-row>
  </div>
</template>

<script setup>
import { ref } from "vue";

const experiences = ref([
  {
    company: "XX科技有限公司",
    position: "高级前端开发工程师",
    period: "2020 - 至今",
    description: "负责公司核心产品的前端开发工作，带领团队完成多个重要项目。",
  },
  {
    company: "YY互联网公司",
    position: "前端开发工程师",
    period: "2018 - 2020",
    description: "参与电商平台的开发，负责用户界面优化和性能提升。",
  },
  {
    company: "ZZ科技创业公司",
    position: "初级前端开发工程师",
    period: "2016 - 2018",
    description: "参与公司产品的前端开发，负责页面实现和组件开发。",
  },
]);
</script>

<style scoped>
.about {
  max-width: 1200px;
  margin: 0 auto;
  padding: 2rem;
}

.profile-section {
  text-align: center;
  margin-bottom: 4rem;
}

.profile-section .el-avatar {
  margin-bottom: 2rem;
}

.bio {
  font-size: 1.2rem;
  color: #666;
  max-width: 800px;
  margin: 0 auto;
  line-height: 1.6;
}

.experience-section {
  margin-bottom: 4rem;
}

h2 {
  text-align: center;
  margin-bottom: 2rem;
}

.el-timeline {
  margin-top: 2rem;
}

.contact-section .el-card {
  text-align: center;
  margin-bottom: 1rem;
}

.contact-section i {
  font-size: 2rem;
  color: #409eff;
  margin-bottom: 1rem;
}

.contact-section h3 {
  margin: 1rem 0;
}
</style> 