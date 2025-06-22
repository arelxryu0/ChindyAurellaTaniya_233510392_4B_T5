<template>
  <nav class="navbar">
    <div class="brand">Toko Online Obat Sehat</div>
    <div class="links">
      <router-link to="/">Home</router-link>
      <router-link to="/product">Product</router-link>
      <router-link to="/contact">Contact</router-link>
    </div>
  </nav>
</template>

<style scoped>
.navbar {
  background: linear-gradient(to right, #81c784, #4db6ac); /* hijau daun ke turquoise */
  color: white;
  padding: 1rem 2rem;
  display: flex;
  justify-content: space-between;
  align-items: center;
  box-shadow: 0 4px 12px rgba(0, 0, 0, 0.15);
  position: sticky;
  top: 0;
  z-index: 10;
  border-bottom: 3px solid #a5d6a7; /* garis bawah hijau lembut */
}

.brand {
  font-size: 1.8rem;
  font-weight: bold;
  letter-spacing: 1px;
  color: #e8f5e9;
  text-shadow: 1px 1px 2px #388e3c99; /* bayangan hijau tua */
}

.links {
  display: flex;
  gap: 1.5rem;
}

.links a {
  color: #e8f5e9;
  text-decoration: none;
  font-weight: 600;
  font-size: 1rem;
  position: relative;
  transition: color 0.3s ease;
}

.links a::after {
  content: "";
  position: absolute;
  bottom: -5px;
  left: 0;
  width: 0%;
  height: 2px;
  background: #c8e6c9;
  transition: width 0.3s ease;
  border-radius: 2px;
}

.links a:hover::after {
  width: 100%;
}

.links a:hover {
  color: #c8e6c9;
}
</style>