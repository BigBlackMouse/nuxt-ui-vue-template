<route lang="yaml">
meta:
  layout: false
</route>

<template>
  <UError
    :error="{
      statusCode: 404,
      statusMessage: 'Page not found',
      message: 'The page you are looking for does not exist.'
    }"
  >
    <!-- 自定义按钮 -->
    <template #links>
      <UButton color="primary" size="lg" @click="goToHome">
        Back to home
      </UButton>
    </template>
  </UError>
</template>

<script setup>
// 用 Vue Router 原生方法！
import { useRouter } from 'vue-router'

const router = useRouter()

const goToHome = () => {
  // 直接跳首页！
  router.push('/')
}
</script>
