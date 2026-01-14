<template>
  <div class="about">
    <h1 class="text-center text-primary mb-4">关于我们</h1>
    <div class="about-content card shadow-sm">
      <div class="card-body">
        <p class="lead">我们是一个专注于提供优质技术服务的团队。我们致力于使用最新的技术栈，为客户提供最佳解决方案。</p>
        <div class="team-section mt-5">
          <h2 class="text-primary mb-4">我们的团队</h2>
          <div class="team-members row g-4">
            <div class="col-md-4">
              <div class="team-member card h-100 text-center">
                <div class="card-body">
                  <div class="avatar mx-auto mb-3">张三</div>
                  <h3 class="h5 card-title">技术总监</h3>
                  <p class="card-text text-muted">10年开发经验</p>
                </div>
              </div>
            </div>
            <div class="col-md-4">
              <div class="team-member card h-100 text-center">
                <div class="card-body">
                  <div class="avatar mx-auto mb-3">李四</div>
                  <h3 class="h5 card-title">前端工程师</h3>
                  <p class="card-text text-muted">Vue 专家</p>
                </div>
              </div>
            </div>
            <div class="col-md-4">
              <div class="team-member card h-100 text-center">
                <div class="card-body">
                  <div class="avatar mx-auto mb-3">王五</div>
                  <h3 class="h5 card-title">后端工程师</h3>
                  <p class="card-text text-muted">全栈开发</p>
                </div>
              </div>
            </div>
          </div>
        </div>
      </div>
    </div>
    <Counter />
  </div>
</template>

<script setup>
import Counter from '../components/Counter.vue'
</script>

<style scoped>
.avatar {
  width: 80px;
  height: 80px;
  background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
  color: white;
  display: flex;
  align-items: center;
  justify-content: center;
  border-radius: 50%;
  font-size: 1.5rem;
  font-weight: bold;
}
</style>
