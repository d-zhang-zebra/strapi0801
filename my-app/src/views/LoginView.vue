<template>
  <div class="login">
    <el-form label-position="top" label-width="100px" style="width: 400px">
      <el-form-item label="Email">
        <el-input />
      </el-form-item>
      <el-form-item label="Password">
        <el-input />
      </el-form-item>
      <el-form-item>
        <el-button type="primary" @click="goTo('list')">Submit</el-button>
      </el-form-item>
    </el-form>
  </div>
</template>

<script setup>
import { useRouter } from 'vue-router'
const router = useRouter()
const goTo = (name) => {
  router.push({ name })
}
</script>

<style scoped>
.login {
  line-height: 1.5;
  width: 100vw;
  display: flex;
  justify-content: center;
  align-items: center;
  /* background: greenyellow; */
  height: 80vh;
}
</style>