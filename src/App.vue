<script setup>
import HelloWorld from './components/HelloWorld.vue'
</script>

<template>
  <div>
    <nav class="p-4 space-x-4">
      <router-link to="/">首頁</router-link>
      <router-link to="/about">關於</router-link>
      <router-link to="/dashboard">儀表板</router-link>
    </nav>
    <router-view />
  </div>
</template>

<style scoped>
nav {
  width: 100%;
  height: 70px;
  background: aliceblue;
  display: flex;
  justify-content: space-evenly;
  align-items: center;
}
</style>
