<template>
  <div class="app">
    <nav class="navbar navbar-expand-lg navbar-dark bg-primary">
      <div class="container">
        <router-link class="navbar-brand" to="/">Vue 首页</router-link>
        <button
          class="navbar-toggler"
          type="button"
          data-bs-toggle="collapse"
          data-bs-target="#navbarNav"
          aria-controls="navbarNav"
          aria-expanded="false"
          aria-label="Toggle navigation"
        >
          <span class="navbar-toggler-icon"></span>
        </button>
        <div class="collapse navbar-collapse" id="navbarNav">
          <ul class="navbar-nav ms-auto">
            <li class="nav-item">
              <router-link class="nav-link" to="/">首页</router-link>
            </li>
            <li class="nav-item">
              <router-link class="nav-link" to="/about">关于</router-link>
            </li>
            <li class="nav-item">
              <router-link class="nav-link" to="/products">产品</router-link>
            </li>
            <li class="nav-item">
              <router-link class="nav-link" to="/contact">联系我们</router-link>
            </li>
            <li class="nav-item">
              <router-link class="nav-link" to="/blank">空白页</router-link>
            </li>
          </ul>
        </div>
      </div>
    </nav>
    <main class="main-content py-4">
      <div class="container">
        <router-view></router-view>
      </div>
    </main>
    <footer class="footer bg-dark text-white text-center py-3">
      <div class="container">
        <p class="mb-0">&copy; 2024 Vue 首页. 保留所有权利.</p>
      </div>
    </footer>
  </div>
</template>

<script setup></script>

<style scoped>
.app {
  min-height: 100vh;
  display: flex;
  flex-direction: column;
}

.main-content {
  flex: 1;
}

.nav-link.router-link-active {
  font-weight: bold;
}
</style>
