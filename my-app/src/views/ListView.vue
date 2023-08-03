<template>
  <div class="list">
    <img src="https://thumb.ac-illust.com/94/947f32ad89b133b86b78879928725483_t.jpeg" alt="">
    <h1>Welcome!</h1>
    <nav>
      <li v-for="item in [1, 2, 3]" :key="item">
        <el-button type="primary" round>category-{{ item }}</el-button>
      </li>
    </nav>
    <ul>
      <li v-for="item in list" :key="item">
        <img src="../assets/logo.svg" alt="">
        <h2>product name</h2>
        <!-- <p>description</p> -->
        <p>price:10</p>
        <!-- <button>add to cart</button> -->
        <div class="df jcc aic">
          <el-button type="primary" @click="goTo('detail')">add to cart</el-button>
        </div>
      </li>
    </ul>
  </div>
</template>

<script setup>
import { ref } from 'vue'
import { useRouter } from 'vue-router'
const router = useRouter()
const list = ref([1, 2, 3, 4, 5, 6, 7])
const goTo = (name) => {
  router.push({ name })
}
</script>

<style scoped>
.list {
  width: 100vw;
}

.list>img {
  display: block;
  margin: 0 auto;
}
h1{
  text-align: center;
}

nav {
  display: flex;
  justify-content: center;
}

ul {
  display: flex;
  flex-wrap: wrap;
}

li {
  width: 200px;
  margin: 20px;
}

li>img {
  display: block;
  width: 100%;
  background: gray;
  margin-bottom: 10px;
}

p {
  margin: 10px 0;
}
</style>
