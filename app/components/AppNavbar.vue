<template>
  <nav class="navbar">
    <NuxtLink to="/" class="logo-wrap">
      <img src="/images/logo_asand3.png" alt="Logo ASANDTT" class="logo-img" />
    </NuxtLink>

    <ul class="nav-links">
      <li><NuxtLink to="/">Accueil</NuxtLink></li>
      <li><NuxtLink to="/association">L'association</NuxtLink></li>
      <li><NuxtLink to="/competitions">Compétitions</NuxtLink></li>
      <li><NuxtLink to="/open-marseille">Open de Marseille</NuxtLink></li>
      <li><NuxtLink to="/promotion">Promotion</NuxtLink></li>
      <li><NuxtLink to="/contact" class="nav-cta">Nous contacter</NuxtLink></li>
    </ul>

    <!-- Burger -->
    <button class="burger" @click="menuOpen = !menuOpen" :class="{ open: menuOpen }" aria-label="Menu">
      <span></span>
      <span></span>
      <span></span>
    </button>

    <!-- Menu mobile -->
    <div class="mobile-menu" :class="{ open: menuOpen }">
      <ul>
        <li><NuxtLink to="/" @click="menuOpen = false">Accueil</NuxtLink></li>
        <li><NuxtLink to="/association" @click="menuOpen = false">L'association</NuxtLink></li>
        <li><NuxtLink to="/competitions" @click="menuOpen = false">Compétitions</NuxtLink></li>
        <li><NuxtLink to="/open-marseille" @click="menuOpen = false">Open de Marseille</NuxtLink></li>
        <li><NuxtLink to="/promotion" @click="menuOpen = false">Promotion</NuxtLink></li>
        <li><NuxtLink to="/contact" class="mobile-cta" @click="menuOpen = false">Nous contacter</NuxtLink></li>
      </ul>
    </div>
  </nav>
</template>

<script setup>
import { ref } from 'vue'
const menuOpen = ref(false)
</script>

<style scoped>
.navbar {
  background: #fff;
  border-bottom: 0.5px solid #e8edf3;
  padding: 0 5rem;
  display: flex;
  align-items: center;
  justify-content: space-between;
  height: 120px;
  position: sticky;
  top: 0;
  z-index: 100;
}
.logo-wrap {
  display: flex;
  align-items: center;
  gap: 11px;
  text-decoration: none;
  flex-shrink: 0;
}
.logo-img {
  height: 100px;
  width: auto;
  object-fit: contain;
}
.nav-links {
  display: flex;
  align-items: center;
  gap: 32px;
  list-style: none;
  position: absolute;
  left: 55%;
  transform: translateX(-50%);
}
.nav-links a {
  font-family: 'Barlow Condensed', sans-serif;
  font-size: 16px;
  letter-spacing: 2.5px;
  text-transform: uppercase;
  color: #1455A4;
  text-decoration: none;
  padding: 8px 18px;
  border-radius: 7px;
  transition: all 0.15s ease;
  font-weight: 600;
}
.nav-links li {
  display: flex;
  align-items: center;
  justify-content: center;
}
.nav-links a:hover {
  background: #f0f5fb;
  color: #0f3f85;
}
.nav-links a.router-link-active {
  color: #0f3f85;
}
.nav-cta {
  background: #3293d4 !important;
  color: #fff !important;
  border-radius: 20px !important;
  padding: 12px 28px !important;
  white-space: nowrap !important;
  font-size: 16px !important;
}
.nav-cta:hover {
  background: #0f3f85 !important;
  color: #fff !important;
}

/* BURGER */
.burger {
  display: none;
  flex-direction: column;
  justify-content: center;
  gap: 5px;
  background: none;
  border: none;
  cursor: pointer;
  padding: 8px;
  z-index: 200;
}
.burger span {
  display: block;
  width: 24px;
  height: 2px;
  background: #0e3471;
  border-radius: 2px;
  transition: all 0.3s ease;
  transform-origin: center;
}
.burger.open span:nth-child(1) {
  transform: translateY(7px) rotate(45deg);
}
.burger.open span:nth-child(2) {
  opacity: 0;
  transform: scaleX(0);
}
.burger.open span:nth-child(3) {
  transform: translateY(-7px) rotate(-45deg);
}

/* MENU MOBILE */
.mobile-menu {
  display: none;
  position: fixed;
  top: 120px;
  left: 0;
  right: 0;
  bottom: 0;
  background: #fff;
  z-index: 99;
  padding: 2rem 2rem;
  transform: translateX(100%);
  transition: transform 0.35s cubic-bezier(0.25, 0.46, 0.45, 0.94);
}
.mobile-menu.open {
  transform: translateX(0);
}
.mobile-menu ul {
  list-style: none;
  display: flex;
  flex-direction: column;
  gap: 0;
  padding: 0;
  margin: 0;
}
.mobile-menu ul li a {
  display: block;
  font-family: 'Barlow Condensed', sans-serif;
  font-size: 22px;
  font-weight: 600;
  letter-spacing: 2px;
  text-transform: uppercase;
  color: #0e3471;
  text-decoration: none;
  padding: 1.1rem 0;
  border-bottom: 0.5px solid #e8edf3;
  transition: color 0.15s ease;
}
.mobile-menu ul li a:hover {
  color: #3293d4;
}
.mobile-cta {
  display: inline-block !important;
  margin-top: 1.5rem;
  background: #3293d4 !important;
  color: #fff !important;
  border-radius: 20px !important;
  padding: 14px 32px !important;
  border-bottom: none !important;
  font-size: 16px !important;
  text-align: center;
}
.mobile-cta:hover {
  background: #0f3f85 !important;
}

/* RESPONSIVE */
@media (max-width: 900px) {
  .navbar {
    padding: 0 1.5rem;
    height: 80px;
  }
  .logo-img {
    height: 65px;
  }
  .nav-links {
    display: none;
  }
  .burger {
    display: flex;
  }
  .mobile-menu {
    display: block;
    top: 80px;
  }
}
</style>