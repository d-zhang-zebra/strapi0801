<template>
  <div class="detail">
    <li>
      <div class="t">
        <div class="l"><img src="../assets/logo.svg" alt=""></div>
        <div class="r">
          <h2>product name</h2>
          <p>description</p>
          <p>price:10</p>
          <div class="df jcc aic">
            <el-button type="primary" @click="goTo('order')">add to cart</el-button>
          </div>
        </div>
      </div>
      <p>description</p>
      <div class="b">
        <img v-for="item in [1, 2, 3]" :key="item"
          src="https://thumb.ac-illust.com/94/947f32ad89b133b86b78879928725483_t.jpeg" alt="">
      </div>
    </li>
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
.detail {
  text-align: center;
}

li {
  width: 80vw;
  margin: 0 auto;
}

.t {
  display: flex;
}

.l {
  width: 200px;
  margin: 20px;
}

.l>img {
  display: block;
  width: 100%;
  background: gray;
  margin-bottom: 10px;
}

.l p {
  margin: 10px 0;
}

.b>img {
  border: 1px solid red;
  display: block;
  width: 100%;
}</style>
