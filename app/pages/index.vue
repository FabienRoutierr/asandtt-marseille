<script setup>
import { ref, onMounted, onUnmounted } from 'vue'

definePageMeta({ layout: 'default' })

useSeoMeta({
  title: 'ASANDTT Marseille — Tennis de table',
  description: 'Club de tennis de table à Marseille. Tous niveaux, tous âges. Loisir et compétition.',
})

// --- STATS COUNTER ---
const statsSection = ref(null)
const counts = ref({ tables: 0, licencies: 0, equipes: 0, ans: 0 })
const targets = { tables: 20, licencies: 200, equipes: 8, ans: 40 }

function animateCount(key, target, duration = 2000) {
  const start = performance.now()
  const update = (now) => {
    const elapsed = now - start
    const progress = Math.min(elapsed / duration, 1)
    const eased = 1 - Math.pow(1 - progress, 3)
    counts.value[key] = Math.floor(eased * target)
    if (progress < 1) requestAnimationFrame(update)
    else counts.value[key] = target
  }
  requestAnimationFrame(update)
}

// --- PARTENAIRES CAROUSEL ---
const partnerTrack = ref(null)
let autoplayInterval = null
let isDragging = false
let startX = 0
let currentTranslate = 0
let dragStartTranslate = 0
let hasDragged = false

const logoCount = 15  // nombre de logos dans UN seul groupe
const logoWidth = 180
const gap = 64
const groupWidth = logoCount * (logoWidth + gap)

function startAutoplay() {
  stopAutoplay()
  autoplayInterval = setInterval(() => {
    currentTranslate += 1
    if (currentTranslate >= groupWidth) {
      currentTranslate -= groupWidth
      if (partnerTrack.value) {
        partnerTrack.value.style.transition = 'none'
        partnerTrack.value.style.transform = `translateX(-${currentTranslate}px)`
      }
      return
    }
    if (partnerTrack.value) {
      partnerTrack.value.style.transition = 'none'
      partnerTrack.value.style.transform = `translateX(-${currentTranslate}px)`
    }
  }, 16)
}

function stopAutoplay() {
  if (autoplayInterval) clearInterval(autoplayInterval)
}

function onDragStart(e) {
  e.preventDefault()
  isDragging = true
  hasDragged = false
  startX = e.type === 'touchstart' ? e.touches[0].clientX : e.clientX
  dragStartTranslate = currentTranslate
  stopAutoplay()
  if (partnerTrack.value) {
    partnerTrack.value.style.transition = 'none'
  }
}

function onDragMove(e) {
  if (!isDragging) return
  e.preventDefault()
  const x = e.type === 'touchmove' ? e.touches[0].clientX : e.clientX
  const diff = startX - x
  if (Math.abs(diff) > 5) hasDragged = true
  currentTranslate = dragStartTranslate + diff
  // Boucle
  if (currentTranslate < 0) currentTranslate += groupWidth
  if (currentTranslate >= groupWidth) currentTranslate -= groupWidth
  if (partnerTrack.value) {
    partnerTrack.value.style.transform = `translateX(-${currentTranslate}px)`
  }
}

function onDragEnd(e) {
  if (!isDragging) return
  isDragging = false
  startAutoplay()
}

function onPartnerClick(e) {
  if (hasDragged) {
    e.preventDefault()
  }
}

onMounted(() => {
  const observer = new IntersectionObserver(
    (entries) => {
      if (entries[0].isIntersecting) {
        animateCount('tables', targets.tables)
        animateCount('licencies', targets.licencies)
        animateCount('equipes', targets.equipes)
        animateCount('ans', targets.ans)
        observer.disconnect()
      }
    },
    { threshold: 0.3 }
  )
  if (statsSection.value) observer.observe(statsSection.value)
  startAutoplay()
})

onUnmounted(() => {
  stopAutoplay()
})
</script>
<template>
  <div>

    <!-- HERO -->
<section class="hero">
  <div class="hero-overlay"></div>
  <img src="/images/photo_pierre.jpg" alt="Gymnase ASANDTT Marseille" class="hero-bg" />
  <div class="hero-content">
    <h1>Le plus grand club<br/><strong>de Marseille</strong></h1>
    <p>Rejoignez l'ASAND — 20 tables, tous niveaux, tous âges. Du loisir à la compétition, dans un grand gymnase au cœur de Marseille.</p>
    <div class="hero-btns">
      <NuxtLink to="/contact" class="btn-primary">Nous rejoindre</NuxtLink>
      <NuxtLink to="/association" class="btn-outline">Découvrir le club</NuxtLink>
    </div>
  </div>
</section>

    <!-- STATS -->
<!-- STATS -->
<div class="stats-row" ref="statsSection">
  <div class="stat">
    <svg class="stat-icon" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="1.5"><rect x="3" y="3" width="18" height="18" rx="2"/><line x1="3" y1="9" x2="21" y2="9"/><line x1="3" y1="15" x2="21" y2="15"/><line x1="9" y1="3" x2="9" y2="21"/><line x1="15" y1="3" x2="15" y2="21"/></svg>
    <span class="stat-n">{{ counts.tables }}</span>
    <span class="stat-l">Tables</span>
  </div>
  <div class="stat">
    <svg class="stat-icon" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="1.5"><path d="M17 21v-2a4 4 0 0 0-4-4H5a4 4 0 0 0-4 4v2"/><circle cx="9" cy="7" r="4"/><path d="M23 21v-2a4 4 0 0 0-3-3.87"/><path d="M16 3.13a4 4 0 0 1 0 7.75"/></svg>
    <span class="stat-n">{{ counts.licencies }}+</span>
    <span class="stat-l">Licenciés</span>
  </div>
  <div class="stat">
    <svg class="stat-icon" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="1.5"><path d="M6 9H4.5a2.5 2.5 0 0 1 0-5H6"/><path d="M18 9h1.5a2.5 2.5 0 0 0 0-5H18"/><path d="M4 22h16"/><path d="M10 14.66V17c0 .55-.47.98-.97 1.21C7.85 18.75 7 20.24 7 22"/><path d="M14 14.66V17c0 .55.47.98.97 1.21C16.15 18.75 17 20.24 17 22"/><path d="M18 2H6v7a6 6 0 0 0 12 0V2Z"/></svg>
    <span class="stat-n">{{ counts.equipes }}</span>
    <span class="stat-l">Équipes</span>
  </div>
  <div class="stat">
    <svg class="stat-icon" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="1.5"><circle cx="12" cy="12" r="10"/><polyline points="12 6 12 12 16 14"/></svg>
    <span class="stat-n">{{ counts.ans }}+</span>
    <span class="stat-l">Ans d'histoire</span>
  </div>
</div>

  <!-- LE CLUB -->
<section class="section section-white">
  <div class="section-inner">
    <h2>Pratiquer, progresser, partager</h2>
    <p class="section-intro">Une structure conviviale pour découvrir ou se perfectionner au tennis de table. Débutant ou compétiteur, nous vous accueillons dans une ambiance dynamique.</p>
    <div class="cards-grid">
<NuxtLink to="/competitions" class="card">
  <div class="card-img">
    <img src="/images/photo_mondon.jpeg" alt="Compétitions" draggable="false" />
    <div class="card-img-overlay">
      <h3>Compétitions</h3>
    </div>
  </div>
  <div class="card-body">
    <p>Championnats par équipes et individuels pour tous les niveaux.</p>
  </div>
</NuxtLink>

<NuxtLink to="/inscription" class="card">
  <div class="card-img">
    <img src="/images/photo-lucas.jpg" alt="Entraînements" draggable="false" />
    <div class="card-img-overlay">
      <h3>Entraînements</h3>
    </div>
  </div>
  <div class="card-body">
    <p>Plusieurs créneaux par semaine, du lundi au vendredi.</p>
  </div>
</NuxtLink>

<NuxtLink to="/open-marseille" class="card">
  <div class="card-img">
    <img src="/images/open-marseille.jpg" alt="Open de Marseille" draggable="false" />
    <div class="card-img-overlay">
      <h3>Open de Marseille</h3>
    </div>
  </div>
  <div class="card-body">
    <p>Notre tournoi annuel, ouvert à tous les joueurs classés.</p>
  </div>
</NuxtLink>

<NuxtLink to="/association" class="card">
  <div class="card-img">
    <img src="/images/photo_asand.png" alt="L'association" draggable="false" />
    <div class="card-img-overlay">
      <h3>L'association</h3>
    </div>
  </div>
  <div class="card-body">
    <p>Découvrez notre histoire, nos valeurs et notre engagement.</p>
  </div>
</NuxtLink>
    </div>
    </div>
</section>

    <!-- ACTUALITÉS -->
    <section class="section section-grey">
      <div class="section-inner">
        <h2>Actualités</h2>
        <div class="news-grid">
        <div class="news-card">
  <div class="news-img">
    <img src="/images/photo_asand.png" alt="Inscriptions" draggable="false" />
  </div>
  <div class="news-body">
    <span class="news-tag">Vie du club</span>
    <p class="news-title">Inscriptions ouvertes toute l'année !</p>
    <span class="news-date">11 décembre 2024</span>
  </div>
</div>
<div class="news-card">
  <div class="news-img">
    <img src="/images/photo_asand.png" alt="Réseaux sociaux" draggable="false" />
  </div>
  <div class="news-body">
    <span class="news-tag">Réseaux sociaux</span>
    <p class="news-title">Suivez-nous sur Facebook et Instagram</p>
    <span class="news-date">28 décembre 2021</span>
  </div>
</div>
<div class="news-card">
  <div class="news-img">
    <img src="/images/photo_asand.png" alt="Compétition" draggable="false" />
  </div>
  <div class="news-body">
    <span class="news-tag">Compétition</span>
    <p class="news-title">Résultats de la dernière journée de championnat</p>
    <span class="news-date">À venir</span>
  </div>
</div>
        </div>
      </div>
    </section>

<!-- PARTENAIRES -->
<section class="section section-white partenaires">
  <div class="section-inner-full">
    <h2 style="text-align:center; margin-bottom:2.5rem;">Nos partenaires</h2>
    <div
      class="partners-viewport"
      @mousedown="onDragStart"
      @mousemove="onDragMove"
      @mouseup="onDragEnd"
      @mouseleave="onDragEnd"
      @touchstart="onDragStart"
      @touchmove="onDragMove"
      @touchend="onDragEnd"
    >
<div class="partners-track" ref="partnerTrack">
    <a href="https://www.departement13.fr" target="_blank" rel="noopener noreferrer" @click="onPartnerClick">
    <img src="/images/Logo-département-13.png" alt="Département 13" draggable="false" />
  </a>
  <a href="https://www.marseille.fr" target="_blank" rel="noopener noreferrer" @click="onPartnerClick">
    <img src="/images/logo-ville-de-marseille.jpg" alt="Ville de Marseille" draggable="false" />
  </a>
  <a href="https://www.fftt.com" target="_blank" rel="noopener noreferrer" @click="onPartnerClick">
    <img src="/images/logo-fftt.jpg" alt="FFTT" class="logo-large" draggable="false" />
  </a>
  <a href="https://high-com.fr" target="_blank" rel="noopener noreferrer" @click="onPartnerClick">
    <img src="/images/Logo-HIGHCOM.png" alt="Highcom" draggable="false" />
  </a>
  <a href="https://www.google.com/maps/search/Nanoglou+Radiateurs+Marseille" target="_blank" rel="noopener noreferrer" @click="onPartnerClick">
    <img src="/images/Logo-NANOGLOU.png" alt="Nanoglou" class="logo-small" draggable="false" />
  </a>
  <a href="https://www.groupe-maurin.com" target="_blank" rel="noopener noreferrer" @click="onPartnerClick">
    <img src="/images/Logo-groupe-MAURIN.png" alt="Groupe Maurin" draggable="false" />
  </a>
  <a href="https://www.speedy.fr" target="_blank" rel="noopener noreferrer" @click="onPartnerClick">
    <img src="/images/Logo-SPEEDY.png" alt="Speedy" draggable="false" />
  </a>
  <a href="https://www.agencedusport.fr/" target="_blank" rel="noopener noreferrer" @click="onPartnerClick">
    <img src="/images/Logo-agence-nationale-du-sport.png" alt="Agence Nationale du Sport" draggable="false" />
  </a>
  <a href="https://www.tripadvisor.fr/Restaurant_Review-g187253-d4010930-Reviews-Les_Terrasses_de_St_Mitre-Marseille_Bouches_du_Rhone_Provence_Alpes_Cote_d_Azur.html" target="_blank" rel="noopener noreferrer" @click="onPartnerClick">
    <img src="/images/Logo-terrasses-saint-mitre.png" alt="Terrasses Saint-Mitre" draggable="false" />
  </a>
  <a href="https://www.cornilleau.com" target="_blank" rel="noopener noreferrer" @click="onPartnerClick">
    <img src="/images/Logo-CORNILLEAU.png" alt="Cornilleau" draggable="false" />
  </a>
  <a href="https://www.silver-equipment.com" target="_blank" rel="noopener noreferrer" @click="onPartnerClick">
    <img src="/images/logo-SILVER-EQUIPMENT.jpg" alt="Silver Equipment" draggable="false" />
  </a>
  <a href="https://www.tennisdetableregionsud.fr/index.php/accueil/general/:infos" target="_blank" rel="noopener noreferrer" @click="onPartnerClick">
    <img src="/images/logo_liguepaca.jpg" alt="Ligue PACA" draggable="false" />
  </a>
  <a href="https://www.cd13tt.fr" target="_blank" rel="noopener noreferrer" @click="onPartnerClick">
    <img src="/images/logo-cd13tt.png" alt="CD13TT" draggable="false" />
  </a>
  <a href="https://www.maregionsud.fr" target="_blank" rel="noopener noreferrer" @click="onPartnerClick">
    <img src="/images/LOGO-région-SUD.jpg" alt="Région Sud" draggable="false" />
  </a>
  <a href="https://www.gewo-tt.com/en/" target="_blank" rel="noopener noreferrer" @click="onPartnerClick">
    <img src="/images/logo-gewo.png" alt="Gewo" draggable="false" />
  </a>
  <!-- Duplication pour boucle -->
    <a href="https://www.departement13.fr" target="_blank" rel="noopener noreferrer" @click="onPartnerClick">
    <img src="/images/Logo-département-13.png" alt="Département 13" draggable="false" />
  </a>
  <a href="https://www.marseille.fr" target="_blank" rel="noopener noreferrer" @click="onPartnerClick">
    <img src="/images/logo-ville-de-marseille.jpg" alt="Ville de Marseille" draggable="false" />
  </a>
  <a href="https://www.fftt.com" target="_blank" rel="noopener noreferrer" @click="onPartnerClick">
    <img src="/images/logo-fftt.jpg" alt="FFTT" class="logo-large" draggable="false" />
  </a>
  <a href="https://high-com.fr" target="_blank" rel="noopener noreferrer" @click="onPartnerClick">
    <img src="/images/Logo-HIGHCOM.png" alt="Highcom" draggable="false" />
  </a>
  <a href="https://www.google.com/maps/search/Nanoglou+Radiateurs+Marseille" target="_blank" rel="noopener noreferrer" @click="onPartnerClick">
    <img src="/images/Logo-NANOGLOU.png" alt="Nanoglou" class="logo-small" draggable="false" />
  </a>
  <a href="https://www.groupe-maurin.com" target="_blank" rel="noopener noreferrer" @click="onPartnerClick">
    <img src="/images/Logo-groupe-MAURIN.png" alt="Groupe Maurin" draggable="false" />
  </a>
  <a href="https://www.speedy.fr" target="_blank" rel="noopener noreferrer" @click="onPartnerClick">
    <img src="/images/Logo-SPEEDY.png" alt="Speedy" draggable="false" />
  </a>
  <a href="https://www.agencedusport.fr/" target="_blank" rel="noopener noreferrer" @click="onPartnerClick">
    <img src="/images/Logo-agence-nationale-du-sport.png" alt="Agence Nationale du Sport" draggable="false" />
  </a>
  <a href="https://www.tripadvisor.fr/Restaurant_Review-g187253-d4010930-Reviews-Les_Terrasses_de_St_Mitre-Marseille_Bouches_du_Rhone_Provence_Alpes_Cote_d_Azur.html" target="_blank" rel="noopener noreferrer" @click="onPartnerClick">
    <img src="/images/Logo-terrasses-saint-mitre.png" alt="Terrasses Saint-Mitre" draggable="false" />
  </a>
  <a href="https://www.cornilleau.com" target="_blank" rel="noopener noreferrer" @click="onPartnerClick">
    <img src="/images/Logo-CORNILLEAU.png" alt="Cornilleau" draggable="false" />
  </a>
  <a href="https://www.silver-equipment.com" target="_blank" rel="noopener noreferrer" @click="onPartnerClick">
    <img src="/images/logo-SILVER-EQUIPMENT.jpg" alt="Silver Equipment" draggable="false" />
  </a>
  <a href="https://www.tennisdetableregionsud.fr/index.php/accueil/general/:infos" target="_blank" rel="noopener noreferrer" @click="onPartnerClick">
    <img src="/images/logo_liguepaca.jpg" alt="Ligue PACA" draggable="false" />
  </a>
  <a href="https://www.cd13tt.fr" target="_blank" rel="noopener noreferrer" @click="onPartnerClick">
    <img src="/images/logo-cd13tt.png" alt="CD13TT" draggable="false" />
  </a>
  <a href="https://www.maregionsud.fr" target="_blank" rel="noopener noreferrer" @click="onPartnerClick">
    <img src="/images/LOGO-région-SUD.jpg" alt="Région Sud" draggable="false" />
  </a>
  <a href="https://www.gewo-tt.com/en/" target="_blank" rel="noopener noreferrer" @click="onPartnerClick">
    <img src="/images/logo-gewo.png" alt="Gewo" draggable="false" />
  </a>
</div>
    </div>
  </div>
</section>

  </div>
</template>

<style scoped>

:global(html),
:global(body) {
  overflow-x: hidden;
  max-width: 100%;
}

/* HERO */
.hero {
  position: relative;
  min-height: 860px;
  display: flex;
  align-items: center;
  overflow: hidden;
}
.hero-bg {
  position: absolute;
  inset: 0;
  width: 100%;
  height: 100%;
  object-fit: cover;
  object-position: center;
}
.hero-overlay {
  position: absolute;
  inset: 0;
  background: linear-gradient(
    to right,
    rgba(10, 30, 70, 0.92) 0%,
    rgba(10, 30, 70, 0.75) 20%,
    rgba(10, 30, 70, 0.15) 100%
  );
  z-index: 1;
}
.hero-content {
  position: relative;
  z-index: 2;
  padding: 4rem 5rem;
  max-width: 650px;
}
.hero-badge {
  display: inline-block;
  background: rgba(255,255,255,0.12);
  border: 0.5px solid rgba(255,255,255,0.2);
  color: #c8dff5;
  font-size: 12px;
  letter-spacing: 1.5px;
  text-transform: uppercase;
  padding: 5px 13px;
  border-radius: 20px;
  margin-bottom: 1.5rem;
}
.hero-content h1 {
  font-size: 58px;
  font-weight: 400;
  color: #fff;
  line-height: 1.1;
  margin-bottom: 1.25rem;
  letter-spacing: -0.5px;
}
.hero-content h1 strong {
  font-weight: 800;
  color: #fff;
}
.hero-content p {
  font-size: 17px;
  color: rgba(255,255,255,0.75);
  line-height: 1.7;
  margin-bottom: 2.5rem;
  max-width: 480px;
}
.hero-btns { display: flex; gap: 12px; flex-wrap: wrap; }
.btn-primary {
  background: #fff;
  color: #0d1f3c;
  padding: 13px 30px;
  border-radius: 8px;
  font-size: 14px;
  font-weight: 600;
  text-decoration: none;
  transition: background 0.15s ease;
}
.btn-primary:hover { background: #e8f0fb; }
.btn-outline {
  background: transparent;
  color: #fff;
  padding: 13px 30px;
  border-radius: 8px;
  font-size: 14px;
  font-weight: 500;
  border: 1.5px solid rgba(255,255,255,0.35);
  text-decoration: none;
  transition: background 0.15s ease;
}
.btn-outline:hover { background: rgba(255,255,255,0.08); }
.hero-img { display: none; }
.btn-primary {
  background: #fff;
  color: #0d1f3c;
  padding: 11px 26px;
  border-radius: 8px;
  font-size: 14px;
  font-weight: 500;
  text-decoration: none;
}
.btn-primary:hover { background: #f0f5fb; }
.btn-outline {
  background: transparent;
  color: #fff;
  padding: 11px 26px;
  border-radius: 8px;
  font-size: 14px;
  border: 1px solid rgba(255,255,255,0.25);
  text-decoration: none;
}
.btn-outline:hover { background: rgba(255,255,255,0.06); }
.hero-img {
  width: 42%;
  flex-shrink: 0;
}
.stats-row {
  display: flex;
  justify-content: center;
  margin: 4rem auto 2rem;
  max-width: 1100px;
}
.stat {
  flex: 1;
  max-width: 280px;
  padding: 3.5rem 2rem;
  text-align: center;
  border-right: none;
  display: flex;
  flex-direction: column;
  align-items: center;
  gap: 8px;
  transition: background 0.2s ease;
}
.stat:last-child { border-right: none; }
.stat-icon {
  width: 42px;
  height: 42px;
  color: #0e3471;
  margin-bottom: 8px;
}
.stat-n {
  font-family: 'Barlow Condensed', sans-serif;
  font-size: 52px;
  font-weight: 700;
  color: #0e3471;
  display: block;
  line-height: 1;
  letter-spacing: 1px;
}
.stat-l {
  font-family: 'Montserrat', sans-serif;
  font-size: 14px;
  font-weight: 600;
  color: #8899aa;
  letter-spacing: 2px;
  text-transform: uppercase;
  display: block;
}

/* SECTIONS */
.section { padding: 5rem 2.5rem; }
.section-white { background: #fff; }
.section-grey { background: #f7f9fc; }
.section-inner { max-width: 1100px; margin: 0 auto; }
.section-tag {
  display: inline-block;
  background: #e8f0fb;
  color: #1455A4;
  font-size: 11px;
  letter-spacing: 1.5px;
  text-transform: uppercase;
  padding: 4px 12px;
  border-radius: 20px;
  margin-bottom: 1rem;
}
.section h2 {
  font-size: 40px;
  font-weight: 500;
  color: #0e3471;
  margin-bottom: 0.75rem;
  letter-spacing: -0.3px;
}
.section-intro {
  font-size: 16px;
  color: #5a6a7a;
  line-height: 1.7;
  max-width: 560px;
}

/* Cards */
.cards-grid {
  display: grid;
  grid-template-columns: repeat(2, 1fr);
  gap: 20px;
  margin-top: 2.5rem;
}
.card {
  border-radius: 16px;
  overflow: hidden;
  border: 0.5px solid #e4eaf2;
  background: #fff;
  transition: transform 0.25s ease, box-shadow 0.25s ease;
  box-shadow: 0 4px 16px rgba(10, 30, 70, 0.08);
  cursor: pointer;
  text-decoration: none;
  display: block;
}
.card:hover {
  transform: translateY(-4px);
  box-shadow: 0 16px 40px rgba(10, 30, 70, 0.15);
}
.card-img {
  position: relative;
  height: 320px;
  overflow: hidden;
}
.card-img img {
  width: 100%;
  height: 100%;
  object-fit: cover;
  transition: transform 0.4s ease;
  display: block;
}
.card:hover .card-img img {
  transform: scale(1.05);
}
.card-img-overlay {
  position: absolute;
  inset: 0;
  background: linear-gradient(to top, rgba(8, 20, 55, 0.65) 0%, transparent 60%);
  display: flex;
  align-items: flex-end;
  padding: 1.25rem 1.5rem;
}
.card-img-overlay h3 {
  font-family: 'Barlow Condensed', sans-serif;
  font-size: 28px;
  font-weight: 700;
  color: #fff;
  letter-spacing: 1px;
  text-transform: uppercase;
  margin: 0;
  text-shadow: 0 2px 8px rgba(0,0,0,0.4);
}
.card-body {
  padding: 1.25rem 1.5rem 1.5rem;
  display: flex;
  flex-direction: column;
  gap: 10px;
}
.card-body p {
  font-size: 13px;
  color: #5a6a7a;
  line-height: 1.6;
  margin: 0;
}
.card-btn {
  align-self: flex-start;
  background: #3293d4;
  color: #fff;
  font-size: 12px;
  font-weight: 500;
  padding: 7px 16px;
  border-radius: 20px;
  text-decoration: none;
  letter-spacing: 0.3px;
  transition: background 0.15s ease, box-shadow 0.15s ease;
  box-shadow: 0 4px 12px rgba(20, 85, 164, 0.35);
}
.card-btn:hover {
  background: #0f3f85;
  box-shadow: 0 6px 18px rgba(20, 85, 164, 0.45);
}

/* NEWS */
.news-grid {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(220px, 1fr));
  gap: 16px;
  margin-top: 2.5rem;
}
.news-card {
  background: #fff;
  border: 0.5px solid #e4eaf2;
  border-radius: 14px;
  overflow: hidden;
}
.news-img-placeholder {
  height: 240px;
  background: #e8f0fb;
}
.news-body { padding: 1rem; }
.news-tag {
  font-size: 11px;
  color: #1455A4;
  text-transform: uppercase;
  letter-spacing: 1px;
}
.news-title {
  font-size: 14px;
  font-weight: 500;
  color: #0d1f3c;
  margin: 5px 0 6px;
  line-height: 1.4;
}
.news-date { font-size: 12px; color: #8899aa; }

/* AGENDA */
.agenda-grid {
  display: grid;
  grid-template-columns: 1fr 1fr;
  gap: 14px;
  margin-top: 2rem;
}
.agenda-item {
  background: #f7f9fc;
  border-left: 3px solid #1455A4;
  border-radius: 0 12px 12px 0;
  padding: 1.1rem 1.3rem;
  display: flex;
  align-items: center;
  gap: 1rem;
}
.agenda-date { text-align: center; min-width: 40px; }
.day { font-size: 24px; font-weight: 500; color: #1455A4; display: block; line-height: 1; }
.month { font-size: 11px; color: #8899aa; text-transform: uppercase; letter-spacing: 1px; }
.agenda-info h4 { font-size: 14px; font-weight: 500; color: #0d1f3c; }
.agenda-info p { font-size: 12px; color: #8899aa; margin-top: 3px; }

/* PARTENAIRES */
.section-inner-full {
  max-width: 1100px;
  margin: 0 auto;
  overflow: hidden;
}
.partners-viewport {
  overflow: hidden;
  width: 100%;
  cursor: grab;
  mask-image: linear-gradient(to right, transparent 0%, black 8%, black 92%, transparent 100%);
  -webkit-mask-image: linear-gradient(to right, transparent 0%, black 8%, black 92%, transparent 100%);
}
.partners-viewport:active {
  cursor: grabbing;
}
.partners-track {
  display: flex;
  align-items: center;
  gap: 4rem;
  transition: transform 0.6s cubic-bezier(0.25, 0.46, 0.45, 0.94);
  width: max-content;
  padding: 1rem 0;
}
.partners-track img {
  height: 60px;
  width: 180px;
  object-fit: contain;
  flex-shrink: 0;
  user-select: none;
  pointer-events: none;
}
.partners-track img.logo-large {
  height: 80px;
}
.partners-track img.logo-small {
  height: 40px;
}
.partners-track a {
  display: flex;
  align-items: center;
  flex-shrink: 0;
  cursor: pointer;
}
.partners-track a img {
  width: 180px; /* reprend la largeur existante */
}

/* ============ RESPONSIVE MOBILE ============ */
@media (max-width: 900px) {

  /* HERO */
  .hero {
    min-height: 520px;
    align-items: flex-end;
  }
  .hero-overlay {
    background: linear-gradient(
      to top,
      rgba(10, 30, 70, 0.92) 0%,
      rgba(10, 30, 70, 0.6) 50%,
      rgba(10, 30, 70, 0.2) 100%
    );
  }
  .hero-content {
    padding: 2rem 1.5rem 3rem;
    max-width: 100%;
  }
  .hero-content h1 {
    font-size: 36px;
  }
  .hero-content p {
    font-size: 15px;
    max-width: 100%;
  }
  .hero-btns {
    flex-direction: column;
    gap: 10px;
  }
  .btn-primary, .btn-outline {
    text-align: center;
    padding: 13px 20px;
  }

  /* STATS */
  .stats-row {
    display: grid;
    grid-template-columns: 1fr 1fr;
    margin: 2rem 1rem;
    gap: 0;
    border-radius: 16px;
    overflow: hidden;
  }
  .stat {
    max-width: 100%;
    padding: 2rem 1rem;
  }
  .stat:nth-child(2n) { border-right: none; }
  .stat:nth-child(3), .stat:nth-child(4) { border-bottom: none; }
  .stat-n { font-size: 42px; }
  .stat-l { font-size: 11px; }
  .stat-icon { width: 28px; height: 28px; }

  /* SECTIONS */
  .section { padding: 3rem 1.25rem; }
  .section h2 { font-size: 28px; }
  .section-intro { font-size: 14px; }

  /* CARDS */
  .cards-grid {
    grid-template-columns: 1fr;
    gap: 16px;
  }
  .card-img { height: 220px; }

  /* NEWS */
  .news-grid {
    grid-template-columns: 1fr;
  }

  /* PARTENAIRES */
  .section-inner-full { padding: 0 1rem; }
}
</style>