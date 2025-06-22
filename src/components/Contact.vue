<template>
  <div class="content">
    <h2 class="section-title">Kontak Kami</h2>
    <p>
  Silakan hubungi kami melalui email di
  <strong>admin@tokoonlineobat.id</strong> atau WhatsApp di
  <strong>+62 812 3456 7890</strong>.
</p>
<h3>Form Pengaduan</h3>
<input type="text" v-model="subject" placeholder="Subjek Pengaduan Obat" required />


    <div class="form-section">
      <h3>Form Pengaduan</h3>
      <form @submit.prevent="handleSubmit">
        <input type="email" v-model="email" placeholder="Email Anda" required />
        <input type="text" v-model="subject" placeholder="Subjek Pengaduan" required />
        <textarea v-model="message" placeholder="Tulis pengaduan Anda..." required></textarea>
        <button type="submit">KIRIM</button>
      </form>

      <p v-if="submitted" class="success-msg">Pengaduan Anda telah dikirim. Terima kasih!</p>
    </div>
  </div>
</template>

<script setup>
import { ref } from 'vue'

const email = ref('')
const subject = ref('')
const message = ref('')
const submitted = ref(false)

const handleSubmit = () => {
  submitted.value = true
  email.value = ''
  subject.value = ''
  message.value = ''
}
</script>

<style scoped>
.content {
  background: #f1f8e9; /* hijau sangat muda */
  padding: 2rem;
  max-width: 700px;
  margin: 2rem auto;
  text-align: center;
  font-size: 1rem;
  color: #2e7d32;
  min-height: 100vh;
  border-radius: 12px;
  box-shadow: 0 8px 16px rgba(76, 175, 80, 0.15);
  line-height: 1.6;
}

.section-title {
  font-size: 1.8rem;
  color: #388e3c;
  margin-bottom: 1.2rem;
  text-shadow: 0 1px 2px rgba(255, 255, 255, 0.6);
  letter-spacing: 0.5px;
  position: relative;
  display: inline-block;
}

.section-title::after {
  content: '';
  width: 50%;
  height: 3px;
  background-color: #66bb6a;
  display: block;
  margin: 0.4rem auto 0;
  border-radius: 2px;
}

.form-section {
  margin-top: 2rem;
  text-align: left;
}

.form-section h3 {
  font-size: 1.3rem;
  margin-bottom: 1rem;
  text-align: center;
  color: #43a047;
}

form {
  display: flex;
  flex-direction: column;
  gap: 0.9rem;
}

input,
textarea {
  padding: 0.75rem;
  border: 1px solid #c8e6c9;
  border-radius: 8px;
  font-size: 0.95rem;
  background: #ffffff;
  color: #2c3e50;
  transition: border 0.3s ease;
}

input:focus,
textarea:focus {
  border-color: #81c784;
  outline: none;
}

textarea {
  height: 120px;
  resize: vertical;
}

button {
  background: #66bb6a;
  color: white;
  font-weight: 600;
  border: none;
  padding: 0.75rem;
  border-radius: 8px;
  cursor: pointer;
  transition: background 0.3s ease;
}

button:hover {
  background: #43a047;
}

.success-msg {
  margin-top: 1rem;
  color: #2e7d32;
  font-weight: 500;
  text-align: center;
}
</style>
