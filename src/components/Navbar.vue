<template>
  <nav class="main-nav">
    <div class="brand">
      <img :src="logoImg" alt="CCS Logo" class="logo" />
      <span class="brand-name">College of Computer Studies</span>
    </div>
    <ul class="nav-links">
      <li><RouterLink to="/#hero">Home</RouterLink></li>
      <li><RouterLink to="/#program">Programs</RouterLink></li>
      <li><RouterLink to="/#faculty">Faculty & Staff</RouterLink></li>
      <li><RouterLink to="/#partners">Partners</RouterLink></li>
    </ul>
  </nav>
</template>

<script setup>
import logoImg from '@/assets/images/css-logo.png'

</script>

<style scoped>
.main-nav {
  position: fixed;
  top: 0;
  left: 0;
  width: 100%;
  background-color: #ffffff;
  box-shadow: 0 2px 10px rgba(20, 83, 45, 0.08);
  display: flex;
  align-items: center;
  justify-content: space-between;
  padding: 18px 40px;
  z-index: 99999;
  box-sizing: border-box;
}

.brand {
  display: flex;
  align-items: center;
  gap: 15px;
  flex-shrink: 0;
}

.logo {
  width: 56px;
  height: 56px;
  object-fit: contain;
}

.brand-name {
  font-size: 1.15rem;
  font-weight: 700;
  color: #14532d;
  white-space: nowrap;
}

.nav-links {
  display: flex;
  gap: 30px;
  list-style: none;
  margin: 0;
  padding: 0;
  align-items: center;
}

.nav-links a {
  text-decoration: none;
  color: #333;
  font-weight: 600;
  font-size: 1rem;
  padding-bottom: 4px;
  border-bottom: 2px solid transparent;
  transition: all 0.2s ease;
  white-space: nowrap;
}

.nav-links a:hover,
.nav-links a.router-link-active {
  color: #14532d;
}

@media (max-width: 900px) {
  .main-nav {
    padding: 15px 20px;
  }

  .nav-links {
    position: absolute;
    top: 100%;
    left: 0;
    right: 0;
    background-color: #ffffff;
    flex-direction: column;
    gap: 0;
    max-height: 0;
    overflow: hidden;
    transition: max-height 0.3s ease;
    box-shadow: 0 4px 10px rgba(20, 83, 45, 0.1);
  }

  .nav-links.open {
    max-height: 300px;
  }

  .nav-links li {
    width: 100%;
  }

  .nav-links a {
    display: block;
    padding: 15px 25px;
    border-bottom: 1px solid #f0f0f0;
  }

  .nav-links a:hover {
    background-color: #f0fdf4;
  }

  .logo {
    width: 44px;
    height: 44px;
  }

  .brand-name {
    font-size: 1rem;
  }
}

@media (max-width: 480px) {
  .brand-name {
    font-size: 0.9rem;
  }

  .logo {
    width: 38px;
    height: 38px;
  }

  .main-nav {
    padding: 12px 15px;
  }
}
</style>