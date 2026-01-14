<template>
  <div class="blank">
    <div class="blank-content">
      <h1 class="text-center text-muted">空白页</h1>
      <p class="text-center text-muted">这是一个空白页面</p>
    </div>
    <Counter />
  </div>
</template>

<script setup>
import Counter from '../components/Counter.vue'
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
