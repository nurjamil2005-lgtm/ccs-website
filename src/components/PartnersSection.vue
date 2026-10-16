<template>
  <section class="partners" id="partners">
    <div class="container">
      <div class="section-header">
        <p class="subheading">Industry Connections</p>
        <h2>Partners & Memberships</h2>
        <div class="gold-line"></div>
      </div>
      <p class="intro">Leading organizations supporting our students' growth and career development</p>
      <div class="partners-grid">
        <div class="partner-card" v-for="(p, i) in partners" :key="i">
          <img :src="getImg(p.file)" :alt="p.name" />
          <h4>{{ p.name }}</h4>
        </div>
      </div>
    </div>
  </section>
</template>

<script setup>
import { ref } from 'vue'

const getImg = (filename) => new URL(`/src/assets/images/${filename}`, import.meta.url).href

const partners = ref([
  { name: 'Oracle', file: 'oracle.png' },
  { name: 'Cisco', file: 'cisco.png' },
  { name: 'Acer', file: 'acer.jpg' },
  { name: 'Huawei', file: 'huawei.jpg' }
])
</script>

<style scoped>
.partners {
  padding: 6rem 3rem;
  background: #ffffff;
  scroll-margin-top: 80px;
}
.container {
  max-width: 1400px;
  margin: 0 auto;
  text-align: center;
  width: 100%;
}
.section-header {
  margin-bottom: 1.5rem;
}
.subheading {
  color: #b8860b;
  font-weight: 600;
  letter-spacing: 2px;
  margin: 0 0 0.8rem;
  font-size: 1.4rem;
}
h2 {
  color: #14532d;
  font-size: 3rem;
  margin: 0 0 0.5rem;
}
.gold-line {
  width: 120px;
  height: 4px;
  background: #b8860b;
  margin: 0 auto 2rem;
}
.intro {
  color: #475569;
  font-size: 1.2rem;
  max-width: 800px;
  margin: 0 auto 4rem;
}
.partners-grid {
  display: grid;
  grid-template-columns: repeat(4, 1fr);
  gap: 3rem;
  width: 100%;
}
.partner-card {
  background: #f8fafc;
  border-radius: 20px;
  padding: 3rem;
  transition: transform 0.2s ease;
  height: 100%;
}
.partner-card:hover {
  transform: translateY(-8px);
}
.partner-card img {
  width: 120px;
  height: 120px;
  object-fit: contain;
  margin-bottom: 1.5rem;
}
.partner-card h4 {
  color: #14532d;
  font-size: 1.3rem;
  margin: 0;
}
@media (max-width: 900px) {
  .partners-grid {
    grid-template-columns: repeat(2, 1fr);
  }
}
@media (max-width: 500px) {
  .partners-grid {
    grid-template-columns: 1fr;
  }
}
</style>