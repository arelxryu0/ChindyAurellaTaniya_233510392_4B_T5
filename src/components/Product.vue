<template>
  <div class="product-page">
    <h2 class="section-title">Produk Obat</h2>
    <ProductCards />
    <div class="basket">
      <h3>Keranjang Belanja</h3>
      <p>Total: Rp0</p>
      <button class="checkout-btn">CHECKOUT</button>
    </div>
  </div>
</template>

<script setup>
import ProductCards from './ProductCards.vue'
</script>

<style scoped>
.product-page {
  background: url('https://i.pinimg.com/736x/6d/d7/00/6dd70015aa116d1575bf558449d3ed5b.jpg') repeat;
  background-size: 300px;
  padding: 2rem;
  text-align: center;
  min-height: 100vh;
  color: #003c8f;
}

.section-title {
  font-size: 2.2rem;
  color: #000000;
  margin-bottom: 2rem;
  text-shadow: 1px 1px 3px #ffffffcc;
  letter-spacing: 1.2px;
  position: relative;
  display: inline-block;
  animation: fadeSlideUp 1s ease-out;
}

.section-title::after {
  content: '';
  width: 70%;
  height: 4px;
  background-color: #000000;
  display: block;
  margin: 0.5rem auto 0;
  border-radius: 2px;
}

@keyframes fadeSlideUp {
  0% {
    opacity: 0;
    transform: translateY(20px) scale(0.95);
  }
  100% {
    opacity: 1;
    transform: translateY(0) scale(1);
  }
}

.basket {
  margin-top: 3rem;
  background: rgba(255, 255, 255, 0.9);
  padding: 1.5rem;
  border-radius: 12px;
  box-shadow: 0 4px 12px rgba(0, 0, 0, 0.1);
  display: inline-block;
}

.checkout-btn {
  margin-top: 1rem;
  padding: 0.8rem 2rem;
  font-size: 1rem;
  font-weight: bold;
  background: #00c853;
  color: white;
  border: none;
  border-radius: 8px;
  cursor: pointer;
  transition: background 0.3s ease, transform 0.2s;
}

.checkout-btn:hover {
  background: #009624;
  transform: scale(1.05);
}
</style>

