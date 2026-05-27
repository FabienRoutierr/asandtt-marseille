<template>
  <nav class="navbar">
    <NuxtLink to="/" class="logo-wrap">
      <img src="/images/logo_asand.png" alt="Logo ASANDTT" class="logo-img" />
      <div>
        <span class="logo-name">ASANDTT Marseille</span>
        <span class="logo-sub">Tennis de table</span>
      </div>
    </NuxtLink>

    <ul class="nav-links">
      <li><NuxtLink to="/">Accueil</NuxtLink></li>
      <li><NuxtLink to="/association">L'association</NuxtLink></li>
      <li><NuxtLink to="/competitions">Compétitions</NuxtLink></li>
      <li><NuxtLink to="/open-marseille">Open de Marseille</NuxtLink></li>
      <li><NuxtLink to="/promotion">Promotion</NuxtLink></li>
      <li><NuxtLink to="/contact" class="nav-cta">Nous contacter</NuxtLink></li></ul>
  </nav>
</template>

<script setup>
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
  height: 44px;
  width: auto;
  object-fit: contain;
}
.logo-name {
  font-size: 16px;
  font-weight: 500;
  color: #0d1f3c;
  letter-spacing: -0.2px;
  display: block;
}
.logo-sub {
  font-size: 11px;
  color: #8899aa;
  letter-spacing: 1.2px;
  text-transform: uppercase;
  display: block;
}
.nav-links {
  display: flex;
  align-items: center;
  gap: 8px;
  list-style: none;
  position: absolute;
  left: 50%;
  transform: translateX(-50%);
}
.nav-links a {
  font-size: 15px;
  letter-spacing: 1.2px;
  text-transform: uppercase;
  color: #1455A4;
  text-decoration: none;
  padding: 8px 18px;
  border-radius: 7px;
  transition: all 0.15s ease;
  font-weight: 700;
}
.nav-links a:hover {
  background: #f0f5fb;
  color: #0f3f85;
}
.nav-links a.router-link-active {
  color: #0f3f85;
  background: #e8f0fb;
}
.nav-cta {
  background: #1455A4 !important;
  color: #fff !important;
  border-radius: 20px !important;
  padding: 10px 22px !important;
}
.nav-cta:hover {
  background: #0f3f85 !important;
  color: #fff !important;
}
</style>