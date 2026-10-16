<template>
  <section class="faculty" id="faculty">
    <div class="container">
      <div class="section-header">
        <p class="subheading">The People Behind CCS</p>
        <h2>Faculty & Staff</h2>
        <div class="gold-line"></div>
      </div>
      <div class="group">
        <h3 class="group-title">College Dean</h3>
        <div class="card-row single">
          <div class="person-card">
            <img :src="deanImg" alt="Dean Quijano" />
            <h4>Ma. Christina A. Quijano, MSCS</h4>
            <p class="role">College Dean</p>
          </div>
        </div>
      </div>
      <div class="group">
        <h3 class="group-title">Department Heads & Coordinators</h3>
        <div class="card-row">
          <div class="person-card" v-for="(p, i) in heads" :key="i">
            <img :src="getImg(p.img)" :alt="p.name" />
            <h4>{{ p.name }}</h4>
            <p class="role">{{ p.role }}</p>
          </div>
        </div>
      </div>
      <div class="group">
        <h3 class="group-title">Faculty Members</h3>
        <div class="card-row">
          <div class="person-card" v-for="(p, i) in faculty" :key="i">
            <img :src="getImg(p.img)" :alt="p.name" />
            <h4>{{ p.name }}</h4>
            <p class="role">{{ p.duty }}</p>
          </div>
        </div>
      </div>
      <div class="group">
        <h3 class="group-title">Administrative Staff</h3>
        <div class="card-row">
          <div class="person-card" v-for="(p, i) in staff" :key="i">
            <img :src="getImg(p.img)" :alt="p.name" />
            <h4>{{ p.name }}</h4>
            <p class="role">{{ p.position }}</p>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>

<script setup>
import { ref } from 'vue'
import deanImg from '@/assets/images/dean.png'

const getImg = (filename) => new URL(`/src/assets/images/${filename}`, import.meta.url).href

const heads = ref([
  { name: 'Rea P. Balontong, MBA', role: 'Dept Head (IT & IS)', img: 'rea.jpg' },
  { name: 'Marjee Rose B. Parreño, MSCS, MBA', role: 'Coord (BSCS, BSDMIA, MSCS)', img: 'marjee.jpg' },
  { name: 'Ana Mae B. Cantel, MLIS', role: 'Coord (BLIS, MLIS)', img: 'ana.jpg' },
  { name: 'Lennon D. Pajar', role: 'Lab Coordinator', img: 'lennon.jpg' }
])

const faculty = ref([
  { name: 'Leo Paulo B. Beldia', duty: 'BSIT & BSIS', img: 'leo.jpg' },
  { name: 'Pedro Peter Rhys B. Cambronero, MSCS', duty: 'BSCS', img: 'pedro.jpg' },
  { name: 'Lesley Joy L. Dignadice, MBA', duty: 'BSIT & BSIS', img: 'lesley.jpg' },
  { name: 'Rodolfo C. Eregia, Jr', duty: 'BSIT & BSIS', img: 'rod.jpg' },
  { name: 'Donie S. Jardeleza, MSCS', duty: 'BSIT & BSIS', img: 'donie.jpg' },
  { name: 'Antonio M. Montaño, Jr.', duty: 'BSIT & BSIS', img: 'antonio.jpg' },
  { name: 'Rose Leah Joy A. Ojacastro, MSCS', duty: 'BSIT & BSIS', img: 'rose.jpg' },
  { name: 'Ma. Sheila C. Sapul, Ph.D.', duty: 'BSCS', img: 'sheila.jpg' }
])

const staff = ref([
  { name: 'Chrislyn C. Castaño', position: 'Secretary', img: 'chrislyn.jpg' },
  { name: 'A.M.P. Latter P. Taasan', position: 'Lab Technician', img: 'latter.jpg' },
  { name: 'Chriselda Elaine Ador', position: 'Guidance Counselor', img: 'chriselda.jpg' },
  { name: 'Donna May Rivera', position: 'Library Liaison Officer', img: 'donna.png' }
])
</script>

<style scoped>
.faculty {
  padding: 6rem 3rem;
  background: #f0fdf4;
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
.group {
  margin-bottom: 5rem;
}
.group-title {
  color: #14532d;
  font-size: 1.6rem;
  margin-bottom: 2.5rem;
  padding-bottom: 0.8rem;
  border-bottom: 3px solid #dcfce7;
}
.card-row {
  display: grid;
  grid-template-columns: repeat(4, 1fr);
  gap: 2.5rem;
  width: 100%;
}
.card-row.single {
  grid-template-columns: 1fr;
  max-width: 350px;
  margin: 0 auto;
}
.person-card {
  background: #fff;
  border-radius: 20px;
  padding: 2.5rem;
  text-align: center;
  box-shadow: 0 4px 12px rgba(20, 83, 45, 0.08);
  height: 100%;
}
.person-card img {
  width: 140px;
  height: 140px;
  object-fit: cover;
  border-radius: 50%;
  margin-bottom: 1.5rem;
}
.person-card h4 {
  color: #14532d;
  font-size: 1.1rem;
  margin: 0 0 0.6rem;
  line-height: 1.4;
}
.role {
  color: #64748b;
  font-size: 1rem;
  margin: 0;
}
@media (max-width: 900px) {
  .card-row {
    grid-template-columns: repeat(2, 1fr);
  }
}
@media (max-width: 500px) {
  .card-row {
    grid-template-columns: 1fr;
  }
}
</style>