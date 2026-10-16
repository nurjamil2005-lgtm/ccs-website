<template>
  <section class="hero" id="hero">
    <div class="container">
      <div class="hero-content">
        <img :src="logoImg" alt="CCS Logo" class="hero-logo" />
        <h1>College of Computer Studies</h1>
        <p class="motto">Building bridges between gaps — different people, one goal</p>
        <div class="values">
          <span>REMEMBER</span>
          <span>CONNECT</span>
          <span>ENGAGE</span>
          <span>BUILD</span>
          <span>SHARE</span>
        </div>
      </div>
    </div>
  </section>
</template>

<script setup>
import logoImg from '@/assets/images/css-logo.png'
</script>

<style scoped>
.hero {
  min-height: 100vh;
  display: flex;
  align-items: center;
  justify-content: center;
  padding: 6rem 3rem;
  background: linear-gradient(180deg, #f0fdf4 0%, #ffffff 100%);
  text-align: center;
  scroll-margin-top: 100px;
}

.hero-content {
  max-width: 1200px;
  margin: 0 auto;
  width: 100%;
}

.hero-logo {
  width: 260px;
  height: 260px;
  object-fit: contain;
  margin-bottom: 2.5rem;
}

.hero h1 {
  color: #14532d;
  font-size: 4rem;
  margin-bottom: 1.5rem;
  line-height: 1.2;
}

.motto {
  color: #475569;
  font-size: 1.3rem;
  margin-bottom: 3rem;
}

.values {
  display: flex;
  justify-content: center;
  align-items: center;
  gap: 1.8rem;
  flex-wrap: nowrap;
  white-space: nowrap;
}
.values:hover {
  transform: translateY(-8px);
}

.values span {
  color: #14532d;
  font-weight: 900;
  font-size: 1.3rem;
  padding: 0.8rem 1.2rem;
  border-bottom: 3px solid #b8860b;
  letter-spacing: 2px;
}
.values span:hover {
  transform: translateY(-8px);
}

@media (max-width: 900px) {
  .hero h1 {
    font-size: 2.8rem;
  }
  .values {
    gap: 1rem;
  }
  .values span {
    font-size: 1rem;
    padding: 0.6rem 0.8rem;
  }
  .hero-logo {
    width: 200px;
    height: 200px;
  }
}

@media (max-width: 600px) {
  .values {
    flex-wrap: wrap;
  }
}
</style>