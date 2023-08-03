<script setup>
import { RouterLink, RouterView } from 'vue-router'
</script>

<template>
  <header>
    <img alt="Vue logo" class="logo" src="@/assets/logo.svg" width="125" height="125" />
    <div class="wrapper">
      <nav>
        <RouterLink to="/">Home</RouterLink>
        <RouterLink to="/table">table</RouterLink>
        <RouterLink to="/list">list</RouterLink>
        <RouterLink to="/detail">detail</RouterLink>
        <RouterLink to="/order">order</RouterLink>
        <RouterLink to="/login">login</RouterLink>
      </nav>
    </div>
  </header>
  <RouterView />
</template>

<style scoped>
header {
  line-height: 1.5;
  width: 100vw;
  display: flex;
  justify-content: space-between;
  align-items: center;
  padding: 0 100px;

}

nav {
  margin-right: 20px;
  /* background: red; */
}
nav > a{
  margin: 0 40px;
}
</style>