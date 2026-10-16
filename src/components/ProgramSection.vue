<template>
  <section class="programs" id="program">
    <div class="container">
      <div class="section-header">
        <p class="subheading">Academic Programs</p>
        <h2>What We Offer</h2>
        <div class="gold-line"></div>
      </div>
      <div class="program-grid">
        <div class="program-card">
          <img :src="bscsImg" alt="BS Computer Science" />
          <h3>Bachelor of Science in Computer Science</h3>
          <p>Designed for in-depth study of computing — focused on software, hardware, algorithms, and the theoretical foundations of computation.</p>
        </div>
        <div class="program-card">
          <img :src="bsitImg" alt="BS Information Technology" />
          <h3>Bachelor of Science in Information Technology</h3>
          <p>Bridges the gap between computer science and information systems — practical skills in infrastructure, applications, and technology management.</p>
        </div>
        <div class="program-card">
          <img :src="dmiaImg" alt="BS Digital Media & Interactive Arts" />
          <h3>Bachelor of Science in Digital Media & Interactive Arts</h3>
          <p>Where creativity meets technology — animation, game design, digital publishing, and interactive media production.</p>
        </div>
        <div class="program-card">
          <img :src="blisImg" alt="BLIS" />
          <h3>Bachelor of Library & Information Science</h3>
          <p>Four-year program building expertise in information organization, library systems, archiving, and knowledge management.</p>
        </div>
      </div>
    </div>
  </section>
</template>

<script setup>
import bscsImg from '@/assets/images/bscs.png'
import bsitImg from '@/assets/images/bsit.png'
import dmiaImg from '@/assets/images/dmia.png'
import blisImg from '@/assets/images/blis.png'
</script>

<style scoped>
.programs {
  padding: 6rem 3rem;
  background: #ffffff;
  scroll-margin-top: 80px;
}
.container {
  max-width: 1400px;
  margin: 0 auto;
  width: 100%;
}
.section-header {
  text-align: center;
  margin-bottom: 5rem;
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
  margin: 0 auto;
}
.program-grid {
  display: grid;
  grid-template-columns: repeat(2, 1fr);
  gap: 3rem;
  width: 100%;
}
.program-card {
  background: #f8fafc;
  border-radius: 20px;
  padding: 3rem;
  text-align: center;
  transition: transform 0.2s ease;
  height: 100%;
}
.program-card:hover {
  transform: translateY(-8px);
}
.program-card img {
  width: 130px;
  height: 130px;
  object-fit: contain;
  margin-bottom: 2rem;
}
.program-card h3 {
  color: #14532d;
  font-size: 1.5rem;
  margin-bottom: 1.2rem;
  line-height: 1.3;
}
.program-card p {
  color: #475569;
  font-size: 1.1rem;
  line-height: 1.8;
  margin: 0;
}
@media (max-width: 900px) {
  .program-grid {
    grid-template-columns: 1fr;
  }
}
</style>