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
  height: 100px;
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
  gap: 32px;
  list-style: none;
  position: absolute;
  left:55%;
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
  font-stretch: condensed;
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
  background: #e8f0fb;
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
</style>