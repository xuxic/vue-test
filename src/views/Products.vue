<template>
  <div class="products">
    <h1 class="text-center text-primary mb-4">我们的产品</h1>
    <div class="product-grid row g-4">
      <div class="col-lg-4 col-md-6" v-for="product in products" :key="product.id">
        <div class="product-card card h-100 text-center shadow-sm">
          <div class="card-body">
            <div class="product-image mb-3">{{ product.icon }}</div>
            <h3 class="card-title h5">{{ product.name }}</h3>
            <p class="card-text text-muted">{{ product.description }}</p>
            <div class="product-price text-primary fw-bold mb-3">¥{{ product.price }}</div>
            <button class="buy-button btn btn-primary">立即购买</button>
          </div>
        </div>
      </div>
    </div>
    <Counter />
  </div>
</template>

<script setup>
import { ref } from 'vue'
import Counter from '../components/Counter.vue'

const products = ref([
  {
    id: 1,
    name: 'Vue 开发工具包',
    description: '一套完整的 Vue 3 开发工具和组件库',
    price: 299,
    icon: '🛠️'
  },
  {
    id: 2,
    name: 'UI 组件库',
    description: '精美的 Vue 3 UI 组件，开箱即用',
    price: 499,
    icon: '🎨'
  },
  {
    id: 3,
    name: '状态管理方案',
    description: '高效的 Vue 状态管理解决方案',
    price: 199,
    icon: '📦'
  },
  {
    id: 4,
    name: '路由管理器',
    description: '强大的 Vue Router 配置和工具',
    price: 149,
    icon: '🧭'
  },
  {
    id: 5,
    name: '测试工具集',
    description: '完整的 Vue 应用测试解决方案',
    price: 399,
    icon: '🧪'
  },
  {
    id: 6,
    name: '性能优化包',
    description: '提升 Vue 应用性能的专业工具',
    price: 599,
    icon: '⚡'
  }
])
</script>

<style scoped>
.product-image {
  font-size: 4rem;
}

.product-card {
  transition: transform 0.3s, box-shadow 0.3s;
}

.product-card:hover {
  transform: translateY(-5px);
  box-shadow: 0 8px 15px rgba(0, 0, 0, 0.2);
}
</style>
