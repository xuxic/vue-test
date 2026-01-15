<template>
  <div class="home">
    <div class="hero bg-primary text-white text-center p-5 rounded mb-5">
      <div class="container">
        <h1 class="display-4 mb-3">欢迎来到 Vue 首页</h1>
        <p class="lead mb-4">这是一个使用 Vue 3 和 Vue Router 构建的现代化网站</p>
        <button class="btn btn-warning btn-lg" @click="navigateToProducts">探索产品</button>
      </div>
    </div>
    <div class="features">
      <div class="row g-4">
        <div class="col-md-4">
          <div class="card h-100 shadow-sm">
            <div class="card-body">
              <h3 class="card-title text-primary">快速开发</h3>
              <p class="card-text">Vue 3 提供了高效的开发体验和优秀的性能</p>
            </div>
          </div>
        </div>
        <div class="col-md-4">
          <div class="card h-100 shadow-sm">
            <div class="card-body">
              <h3 class="card-title text-primary">组件化</h3>
              <p class="card-text">通过组件化架构构建可维护的应用程序</p>
            </div>
          </div>
        </div>
        <div class="col-md-4">
          <div class="card h-100 shadow-sm">
            <div class="card-body">
              <h3 class="card-title text-primary">响应式设计</h3>
              <p class="card-text">完美适配各种设备和屏幕尺寸</p>
            </div>
          </div>
        </div>
      </div>
    </div>
    <Counter father="Home页面" />
  </div>
</template>

<script setup>
import { useRouter } from 'vue-router'
import Counter from '../components/Counter.vue'

const router = useRouter()

const navigateToProducts = () => {
  router.push('/products')
}
</script>

<style scoped>
.home {
  text-align: center;
}

.hero {
  background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
}

.card {
  transition: transform 0.3s;
}

.card:hover {
  transform: translateY(-5px);
}
</style>
