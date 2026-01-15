<template>
  <div class="counter">
    <div class="counter-container">
      <button @click="decrement" class="btn btn-outline-danger">-</button>
      <span class="counter-value">{{ count }}</span>
      <button @click="increment" class="btn btn-outline-primary">+</button>
    </div>
    <p class="counter-value">当前页面：{{ father }}</p>
  </div>
</template>

<script setup>
import { ref } from "vue";

const props = defineProps({
  father: {
    type: String,
    default: "",
  },
});

const count = ref(0);

const increment = () => {
  count.value++;
};

const decrement = () => {
  if (count.value > 0) {
    count.value--;
  }
};
</script>

<style scoped>
.counter {
  padding: 1rem 0;
}

.counter-container {
  display: flex;
  align-items: center;
  justify-content: center;
  gap: 1rem;
}

.counter-value {
  font-size: 1.5rem;
  font-weight: bold;
  min-width: 3rem;
  text-align: center;
}
</style>
