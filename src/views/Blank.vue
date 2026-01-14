<template>
  <div class="blank">
    <div class="blank-content">
      <h1 class="text-center text-muted">空白页</h1>
      <p class="text-center text-muted">这是一个空白页面</p>
      <router-link to="/contact">联系我们</router-link>
    </div>
  </div>
</template>

<script setup>
</script>

<style scoped>
.blank {
  min-height: 50vh;
  display: flex;
  align-items: center;
  justify-content: center;
}

.blank-content {
  text-align: center;
}
</style>
