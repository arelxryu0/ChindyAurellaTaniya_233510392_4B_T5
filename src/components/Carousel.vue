<template>
  <div class="carousel">
    <div class="slide">💊 Selamat Datang di Toko Online Obat Sehat!</div>
  </div>
</template>

<style scoped>
.carousel {
  display: flex;
  justify-content: center;
  align-items: center;
  height: 100px; /* diperkecil dari 140px */
  margin: 1rem;
  background: #e0f2f1;
  border-radius: 10px;
  box-shadow: 0 3px 8px rgba(0, 0, 0, 0.08);
  padding: 0.8rem 1.5rem; /* padding juga sedikit dikurangi */
  transition: box-shadow 0.3s ease;
}

.carousel:hover {
  box-shadow: 0 5px 14px rgba(0, 0, 0, 0.12);
}

.slide {
  font-size: 1.2rem; /* sedikit lebih kecil dari sebelumnya */
  font-weight: 600;
  color: #388e3c;
  text-align: center;
  animation: fadeSlideUp 0.8s ease-out;
  text-shadow: 0 1px 1px rgba(255, 255, 255, 0.6);
}

@keyframes fadeSlideUp {
  0% {
    opacity: 0;
    transform: translateY(15px);
  }
  100% {
    opacity: 1;
    transform: translateY(0);
  }
}

</style>