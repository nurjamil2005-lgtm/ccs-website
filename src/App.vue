<template>
  <div class="app-wrapper">
    <Navbar />
    <main class="page-content">
      <HomeView />
    </main>
  </div>
</template>

<script setup>
import Navbar from './components/Navbar.vue'
import HomeView from './views/HomeView.vue'
</script>

<style>
* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}
html {
  scroll-behavior: smooth;
}
body {
  font-family: 'Times New Roman', serif;
  background-color: #f0fdf4;
  color: #333;
}
.app-wrapper {
  min-height: 100vh;
  display: flex;
  flex-direction: column;
}
.page-content {
  padding-top: 90px; 
  flex: 1;
}

@media (max-width: 900px) {
  .page-content {
    padding-top: 80px;
  }
}
</style>