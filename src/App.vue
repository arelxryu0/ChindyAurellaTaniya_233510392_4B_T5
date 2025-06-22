<template>
  <div class="app">
    <Navbar />
    <main class="main-content">
      <router-view />
    </main>
    <Footer />
  </div>
</template>

<script setup>
import Navbar from './components/Navbar.vue'
import Footer from './components/Footer.vue'
</script>

<style>
body {
  background: url('https://i.pinimg.com/736x/6d/d7/00/6dd70015aa116d1575bf558449d3ed5b.jpg');
  background-size: 300px;
}


#app,
.app {
  display: flex;
  flex-direction: column;
  min-height: 100vh;
}

.main-content {
  flex: 1;
}

</style>