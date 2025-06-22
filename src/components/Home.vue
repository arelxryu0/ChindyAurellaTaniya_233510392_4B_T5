<template>
  <div class="home-container">
    <Carousel />
    <ProductCards />
  </div>
</template>

<script setup>
import Carousel from './Carousel.vue'
import ProductCards from './ProductCards.vue'
</script>

<style scoped>
.product-page,
.home-container {
  background: url('https://i.pinimg.com/736x/6d/d7/00/6dd70015aa116d1575bf558449d3ed5b.jpg') no-repeat center center;
  background-size: cover;
  min-height: 100vh;
  padding-top: 1rem;
  padding-bottom: 2rem;
}


.section-title {
  font-size: 2rem;
  color: #1976d2;
  margin-bottom: 2rem;
  text-shadow: 1px 1px 2px #ffffffcc;
  letter-spacing: 1px;
  position: relative;
  display: inline-block;
}

.section-title::after {
  content: '';
  width: 60%;
  height: 4px;
  background-color: #1976d2;
  display: block;
  margin: 0.5rem auto 0;
  border-radius: 2px;
}

.basket {
  margin-top: 3rem;
}

.checkout-btn {
  margin-top: 1rem;
  padding: 0.6rem 1.5rem;
  font-weight: bold;
  background: #43a047;
  color: white;
  border: none;
  border-radius: 6px;
  cursor: pointer;
  transition: background 0.3s ease;
}

.checkout-btn:hover {
  background: #2e7d32;
}

</style>
