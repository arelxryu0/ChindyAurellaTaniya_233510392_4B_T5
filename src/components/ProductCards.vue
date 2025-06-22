<template>
  <div class="cards">
    <div class="card" v-for="product in products" :key="product.id">
      <img :src="product.image" alt="product" />
      <h3>{{ product.name }}</h3>
      <p>{{ product.description }}</p>
      <p><strong>Harga:</strong> {{ product.price }}</p>
      <button class="add-btn">TAMBAH KE KERANJANG</button>
    </div>
  </div>
</template>

<script setup>
const products = [
  {
    id: 1,
    name: 'Paracetamol 500mg',
    description: 'Obat penurun demam dan pereda nyeri ringan.',
    price: 'Rp10.000',
    image: 'https://rsum.bandaacehkota.go.id/wp-content/uploads/2025/02/paracetamol.webp'
  },
  {
    id: 2,
    name: 'Vitamin C 1000mg',
    description: 'Suplemen daya tahan tubuh harian.',
    price: 'Rp25.000',
    image: 'https://images-cdn.ubuy.co.id/633ffbaa5a9c8a453729ea76-30-pills-acorbic-c-1000-mg-vittamin-c.jpg'
  },
  {
    id: 3,
    name: 'Salep Kulit Anti Jamur',
    description: 'Obat luar untuk infeksi jamur pada kulit.',
    price: 'Rp15.000',
    image: 'https://res.cloudinary.com/dk0z4ums3/image/upload/v1749605435/attached_image/obat-jamur-kulit-paling-ampuh-di-apotik-5-alodokter.jpg'
  }
]

</script>

<style scoped>
.cards {
  display: flex;
  flex-wrap: wrap;
  justify-content: center;
  gap: 2rem;
  margin-top: 1rem;
}

.card {
  background: #ffffff;
  padding: 1rem;
  width: 260px;
  border-radius: 10px;
  box-shadow: 0 4px 12px rgba(0, 0, 0, 0.1);
  text-align: center;
  transition: transform 0.3s ease;
  font-size: 0.85rem; /* global font-size dalam card */
}

.card:hover {
  transform: translateY(-5px);
}

.card img {
  width: 100%;
  height: 180px;
  object-fit: cover;
  border-radius: 8px;
  margin-bottom: 1rem;
}

.card h3 {
  margin: 0.4rem 0;
  color: #1e88e5;
  font-size: 1.05rem; /* lebih kecil dari sebelumnya */
}

.card p {
  font-size: 0.85rem;
  color: #666;
  margin-bottom: 0.3rem;
}

.add-btn {
  margin-top: 0.8rem;
  background: #ff9800;
  color: white;
  border: none;
  padding: 0.5rem 1rem;
  border-radius: 6px;
  font-weight: 600;
  font-size: 0.85rem;
  cursor: pointer;
  transition: background 0.3s ease;
}

.add-btn:hover {
  background: #ef6c00;
}


</style>
