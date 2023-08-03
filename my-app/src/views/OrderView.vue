<template>
  <div class="order">
    <div class="order-detail">
      <h2>product name</h2>
      <p>description</p>
      <p>price:10</p>
      <div class="df jcc aic">
        <el-button type="primary" @click="goTo('table')">send email</el-button>
      </div>
    </div>
  </div>
</template>

<script setup>
// import { ref } from 'vue'
import { useRouter } from 'vue-router'
const router = useRouter()
// const list = ref([1, 2, 3, 4, 5, 6, 7])
const goTo = (name) => {
  router.push({ name })
}
</script>

<style scoped>
.order-detail{
  text-align: center;
}
</style>
