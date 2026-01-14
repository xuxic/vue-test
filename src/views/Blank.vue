<template>
  <div class="blank">
    <div class="blank-content">
      <h1 class="text-center text-muted">空白页</h1>
      <p class="text-center text-muted">这是一个空白页面</p>
      <Counter />
      <button v-on:click="showMessage = !showMessage">显示/隐藏</button>
      <p v-show="showMessage">Hello Vue!</p>
    </div>
  </div>
</template>

<script setup>
import Counter from "../components/Counter.vue";
import { ref } from "vue";

const showMessage = ref(false);
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
