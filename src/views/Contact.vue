<template>
  <div class="contact">
    <h1 class="text-center text-primary mb-4">联系我们</h1>
    <div class="contact-container row g-4">
      <div class="col-lg-5">
        <div class="contact-info card shadow-sm">
          <div class="card-body">
            <h2 class="text-primary mb-4">联系方式</h2>
            <div class="info-item mb-3">
              <span class="icon me-3">📍</span>
              <span>地址：北京市朝阳区科技园区</span>
            </div>
            <div class="info-item mb-3">
              <span class="icon me-3">📧</span>
              <span>邮箱：contact@example.com</span>
            </div>
            <div class="info-item mb-3">
              <span class="icon me-3">📞</span>
              <span>电话：400-123-4567</span>
            </div>
            <div class="info-item">
              <span class="icon me-3">🕐</span>
              <span>工作时间：周一至周五 9:00-18:00</span>
            </div>
          </div>
        </div>
      </div>
      <div class="col-lg-7">
        <div class="contact-form card shadow-sm">
          <div class="card-body">
            <h2 class="text-primary mb-4">给我们留言</h2>
            <form @submit.prevent="handleSubmit">
              <div class="mb-3">
                <label for="name" class="form-label">姓名</label>
                <input
                  type="text"
                  class="form-control"
                  id="name"
                  v-model="formData.name"
                  required
                />
              </div>
              <div class="mb-3">
                <label for="email" class="form-label">邮箱</label>
                <input
                  type="email"
                  class="form-control"
                  id="email"
                  v-model="formData.email"
                  required
                />
              </div>
              <div class="mb-3">
                <label for="subject" class="form-label">主题</label>
                <input
                  type="text"
                  class="form-control"
                  id="subject"
                  v-model="formData.subject"
                  required
                />
              </div>
              <div class="mb-3">
                <label for="message" class="form-label">留言内容</label>
                <textarea
                  class="form-control"
                  id="message"
                  v-model="formData.message"
                  rows="5"
                  required
                ></textarea>
              </div>
              <button type="submit" class="submit-button btn btn-primary w-100">
                发送留言
              </button>
            </form>
          </div>
        </div>
      </div>
    </div>
    <Counter />
  </div>
</template>

<script setup>
import { ref } from "vue";
import Counter from "../components/Counter.vue";

const formData = ref({
  name: "",
  email: "",
  subject: "",
  message: "",
});

const handleSubmit = () => {
  alert("感谢您的留言！我们会尽快与您联系。");
  formData.value = {
    name: "",
    email: "",
    subject: "",
    message: "",
  };
};
</script>

<style scoped>
.info-item {
  display: flex;
  align-items: center;
}

.icon {
  font-size: 1.5rem;
}
</style>
