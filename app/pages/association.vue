<script setup>
definePageMeta({ layout: 'default' })

useSeoMeta({
  title: 'L\'association — ASANDTT Marseille',
  description: 'Découvrez le club de l\'ASAND, la référence du tennis de table à Marseille depuis 1974.',
})

const bureau = [
  { name: 'Sébastien Malet', role: 'Président', img: '/images/photo_seb.jpeg' },
  { name: 'Richard Monier', role: 'Trésorier', img: '/images/photo_richard.png' },
  { name: 'Jacky Routier', role: 'Secrétaire', img: '/images/photo_jacky.png' },
]

const pratiques = [
  {
    icon: '🏓',
    title: 'Compétition',
    desc: '8 équipes du départemental au national. Les joueurs les mieux classés de Marseille, tous clubs confondus.',
  },
  {
    icon: '😊',
    title: 'Loisir',
    desc: 'Des créneaux sans condition de niveau pour tous les amateurs. La pratique loisir est majoritaire au club.',
  },
  {
    icon: '⭐',
    title: 'Jeunes',
    desc: 'Formation des plus jeunes, notre priorité depuis toujours. Encadrés par notre éducateur sportif.',
  },
  {
    icon: '👩',
    title: 'Féminin',
    desc: 'La pratique féminine est très importante. Des joueuses de tous âges et niveaux, en nombre croissant.',
  },
]
</script>

<template>
  <div>

    <!-- HERO -->
    <section class="hero">
      <div class="hero-overlay"></div>
      <img src="/images/photo_asand.png" alt="Club ASANDTT Marseille" class="hero-bg" />
      <div class="hero-content">
        <span class="hero-badge">Fondé en 1974 · Marseille</span>
        <h1>L'association<br/><strong>ASANDTT</strong></h1>
        <p>La référence du tennis de table à Marseille depuis plus de 50 ans. Ouvert à tous, tous les niveaux, tous les âges.</p>
      </div>
    </section>

    <!-- CHIFFRES CLÉS -->
    <div class="key-stats">
      <div class="key-stat">
        <span class="key-n">1974</span>
        <span class="key-l">Année de création</span>
      </div>
      <div class="key-stat">
        <span class="key-n">200+</span>
        <span class="key-l">Adhérents</span>
      </div>
      <div class="key-stat">
        <span class="key-n">20</span>
        <span class="key-l">Tables</span>
      </div>
      <div class="key-stat">
        <span class="key-n">7–76</span>
        <span class="key-l">Ans, tous les âges</span>
      </div>
    </div>

    <!-- BUREAU -->
    <section class="section section-white">
      <div class="section-inner">
        <h2>Le bureau de l'association</h2>
        <div class="bureau-grid">
          <div v-for="member in bureau" :key="member.name" class="bureau-card">
            <div class="bureau-img">
              <img :src="member.img" :alt="member.name" />
            </div>
            <div class="bureau-info">
              <span class="bureau-role">{{ member.role }}</span>
              <span class="bureau-name">{{ member.name }}</span>
            </div>
          </div>
        </div>
      </div>
    </section>

    <!-- PRÉSENTATION -->
    <section class="section section-grey">
      <div class="section-inner presentation-grid">
        <div class="presentation-text">
          <h2>Un club ouvert à tous depuis 1974</h2>
          <p>Créé en 1974, le club de l'ASAND est la référence du tennis de table à Marseille. Nous sommes le club numéro 1 de la ville à tous les niveaux.</p>
          <p>Le club est ouvert à tous : jeunes et adultes, débutants, loisir ou compétition. Quel que soit votre âge ou votre niveau, vous êtes les bienvenus au gymnase Antonin Artaud.</p>
          <p>Nous avons la chance d'avoir un grand gymnase mis à disposition par la ville de Marseille, 20 tables de qualité et un parking gratuit pour accueillir tous nos adhérents dans les meilleures conditions.</p>
          <div class="info-blocks">
            <div class="info-block">
              <svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="1.5"><circle cx="12" cy="12" r="10"/><polyline points="12 6 12 12 16 14"/></svg>
              <div>
                <strong>Horaires</strong>
                <span>Lun – Ven : 17h30 – 21h · Sam : compétitions</span>
              </div>
            </div>
            <div class="info-block">
              <svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="1.5"><path d="M21 10c0 7-9 13-9 13s-9-6-9-13a9 9 0 0 1 18 0z"/><circle cx="12" cy="10" r="3"/></svg>
              <div>
                <strong>Adresse</strong>
                <span>Gymnase Antonin Artaud · 25 chemin Notre Dame de Consolation · 13013 Marseille</span>
              </div>
            </div>
            <div class="info-block">
              <svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="1.5"><path d="M22 16.92v3a2 2 0 0 1-2.18 2 19.79 19.79 0 0 1-8.63-3.07A19.5 19.5 0 0 1 4.69 12a19.79 19.79 0 0 1-3.07-8.67A2 2 0 0 1 3.6 1.27h3a2 2 0 0 1 2 1.72c.127.96.361 1.903.7 2.81a2 2 0 0 1-.45 2.11L7.91 8.91a16 16 0 0 0 6 6l.95-.95a2 2 0 0 1 2.11-.45c.907.339 1.85.573 2.81.7A2 2 0 0 1 21.73 16.92z"/></svg>
              <div>
                <strong>Contact</strong>
                <span>04 91 78 80 00 · Les inscriptions sont ouvertes toute l'année</span>
              </div>
            </div>
          </div>
        </div>
        <div class="presentation-img">
          <img src="/images/photo_asand.png" alt="Gymnase ASANDTT" />
        </div>
      </div>
    </section>

    <!-- ENCADRANTS -->
    <section class="section section-white">
      <div class="section-inner">
        <h2>Nos cadres techniques</h2>
        <p class="section-intro">Deux encadrants expérimentés, également les deux joueurs les mieux classés de Marseille depuis plus de 20 ans.</p>
        <div class="coaches-grid">
       <div class="coach-card">
  <div class="coach-img">
    <img src="/images/photo_michel2.png" alt="Michel Franquebalme" />
    <div class="coach-img-overlay">
      <h3>Michel FRANQUEBALME</h3>
    </div>
  </div>
  <div class="coach-body">
    <span class="coach-role">Entraîneur principal · CDI temps plein</span>
    <ul class="coach-achievements">
      <li>Entraîneur diplômé d'État depuis plus de 15 ans au club</li>
      <li>Joueur numéroté FFTT depuis plus de 25 ans</li>
      <li>Ancien membre de l'équipe de France jeunes</li>
      <li>Vice-champion d'Europe cadet par équipes</li>
      <li>A évolué en Nationale 1 en individuel et par équipes</li>
    </ul>
  </div>
</div>
<div class="coach-card">
  <div class="coach-img">
    <img src="/images/photo_seb.jpeg" alt="Sébastien Malet" />
    <div class="coach-img-overlay">
      <h3>Sébastien MALET</h3>
    </div>
  </div>
  <div class="coach-body">
    <span class="coach-role">Président · Entraîneur adjoint</span>
    <ul class="coach-achievements">
      <li>Formé au club de l'ASAND</li>
      <li>Membre du club depuis 1996</li>
      <li>Joueur numéroté FFTT depuis 25 ans</li>
      <li>N°1 de la ville de Marseille</li>
      <li>A évolué en Nationale 1 en individuel et par équipes</li>
    </ul>
  </div>
</div>
        
        </div>
      </div>
    </section>

    <!-- PRATIQUES -->
    <section class="section section-grey">
      <div class="section-inner">
        <h2>Un club pour chaque profil</h2>
        <p class="section-intro">Du débutant au compétiteur national, de 7 à 76 ans, l'ASAND accueille tout le monde dans la bonne humeur.</p>
        <div class="pratiques-grid">
          <div v-for="item in pratiques" :key="item.title" class="pratique-card">
            <span class="pratique-icon">{{ item.icon }}</span>
            <h3>{{ item.title }}</h3>
            <p>{{ item.desc }}</p>
          </div>
        </div>
      </div>
    </section>

    <!-- CTA -->
    <section class="cta-section">
      <div class="cta-inner">
        <h2>Rejoignez-nous !</h2>
        <p>Que vous soyez jeune ou adulte, compétiteur ou simple amateur de ping-pong, vous êtes les bienvenus au club de l'ASAND.</p>
        <div class="cta-btns">
          <NuxtLink to="/contact" class="btn-primary">Nous contacter</NuxtLink>
          <a href="https://www.facebook.com" target="_blank" class="btn-outline">Nous suivre</a>
        </div>
      </div>
    </section>

  </div>
</template>

<style scoped>
/* HERO */
.hero {
  position: relative;
  min-height: 520px;
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
  background: linear-gradient(to right, rgba(10,30,70,0.92) 0%, rgba(10,30,70,0.65) 55%, rgba(10,30,70,0.15) 100%);
  z-index: 1;
}
.hero-content {
  position: relative;
  z-index: 2;
  padding: 4rem 5rem;
  max-width: 620px;
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
  font-family: 'Barlow Condensed', sans-serif;
  font-size: 64px;
  font-weight: 400;
  color: #fff;
  line-height: 1.05;
  margin-bottom: 1rem;
  letter-spacing: 0.5px;
  text-transform: uppercase;
}
.hero-content h1 strong { font-weight: 800; }
.hero-content p {
  font-size: 16px;
  color: rgba(255,255,255,0.75);
  line-height: 1.7;
  max-width: 460px;
}

/* KEY STATS */
.key-stats {
  background: #0a1f4e;
  display: flex;
  justify-content: center;
}
.key-stat {
  flex: 1;
  max-width: 240px;
  padding: 2.5rem 2rem;
  text-align: center;
  border-right: 0.5px solid rgba(255,255,255,0.08);
}
.key-stat:last-child { border-right: none; }
.key-n {
  font-family: 'Barlow Condensed', sans-serif;
  font-size: 42px;
  font-weight: 700;
  color: #fff;
  display: block;
  line-height: 1;
}
.key-l {
  font-size: 11px;
  color: rgba(255,255,255,0.5);
  letter-spacing: 1.5px;
  text-transform: uppercase;
  margin-top: 6px;
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
  font-size: 30px;
  font-weight: 500;
  color: #0e3471;
  margin-bottom: 0.75rem;
  letter-spacing: -0.3px;
}
.section-intro {
  font-size: 16px;
  color: #5a6a7a;
  line-height: 1.7;
  max-width: 600px;
  margin-bottom: 2rem;
}

/* BUREAU */
.bureau-grid {
  display: grid;
  grid-template-columns: repeat(3, 1fr);
  gap: 24px;
  margin-top: 2.5rem;
}
.bureau-card {
  border-radius: 16px;
  overflow: hidden;
  border: 0.5px solid #e4eaf2;
  box-shadow: 0 4px 16px rgba(10,30,70,0.07);
  transition: transform 0.25s ease, box-shadow 0.25s ease;
}
.bureau-card:hover {
  transform: translateY(-4px);
  box-shadow: 0 12px 32px rgba(10,30,70,0.12);
}
.bureau-img {
  height: 400px;
  overflow: hidden;
}
.bureau-img img {
  width: 100%;
  height: 100%;
  object-fit: cover;
  object-position: center top;
  transition: transform 0.4s ease;
}
.bureau-card:hover .bureau-img img { transform: scale(1.04); }
.bureau-info {
  padding: 1.25rem 1.5rem;
  display: flex;
  flex-direction: column;
  gap: 4px;
  background: #fff;
}
.bureau-role {
  font-size: 11px;
  color: #1455A4;
  text-transform: uppercase;
  letter-spacing: 1.5px;
  font-weight: 600;
}
.bureau-name {
  font-size: 17px;
  font-weight: 600;
  color: #0d1f3c;
}

/* PRÉSENTATION */
.presentation-grid {
  display: grid;
  grid-template-columns: 1fr 420px;
  gap: 4rem;
  align-items: center;
}
.presentation-text p {
  font-size: 15px;
  color: #5a6a7a;
  line-height: 1.75;
  margin-bottom: 1rem;
}
.info-blocks {
  display: flex;
  flex-direction: column;
  gap: 12px;
  margin-top: 1.5rem;
}
.info-block {
  display: flex;
  align-items: flex-start;
  gap: 12px;
  background: #fff;
  border-radius: 10px;
  padding: 0.9rem 1.1rem;
  border: 0.5px solid #e4eaf2;
}
.info-block svg {
  width: 18px;
  height: 18px;
  color: #1455A4;
  flex-shrink: 0;
  margin-top: 2px;
}
.info-block div {
  display: flex;
  flex-direction: column;
  gap: 2px;
}
.info-block strong {
  font-size: 13px;
  font-weight: 600;
  color: #0d1f3c;
}
.info-block span {
  font-size: 13px;
  color: #5a6a7a;
  line-height: 1.5;
}
.presentation-img {
  border-radius: 16px;
  overflow: hidden;
  height: 480px;
}
.presentation-img img {
  width: 100%;
  height: 100%;
  object-fit: cover;
}

/* COACHES */
.coaches-grid {
  display: grid;
  grid-template-columns: 1fr 1fr;
  gap: 24px;
  margin-top: 2.5rem;
}
.coach-card {
  background: #fff;
  border: 0.5px solid #e4eaf2;
  border-radius: 16px;
  overflow: hidden;
  box-shadow: 0 4px 16px rgba(10,30,70,0.06);
  display: flex;
  flex-direction: column;
}
.coach-img {
  position: relative;
  height: 340px;
  overflow: hidden;
}
.coach-img img {
  width: 100%;
  height: 100%;
  object-fit: cover;
  object-position: center top;
}
.coach-img-overlay {
  position: absolute;
  inset: 0;
  background: linear-gradient(to top, rgba(8,20,55,0.75) 0%, transparent 55%);
  display: flex;
  align-items: flex-end;
  padding: 1.25rem 1.5rem;
}
.coach-img-overlay h3 {
  font-family: 'Barlow Condensed', sans-serif;
  font-size: 26px;
  font-weight: 700;
  color: #fff;
  text-transform: uppercase;
  letter-spacing: 1px;
  margin: 0;
  text-shadow: 0 2px 8px rgba(0,0,0,0.4);
}
.coaches-grid {
  display: grid;
  grid-template-columns: repeat(2, 360px);
  gap: 24px;
  margin-top: 2.5rem;
  justify-content: center;
}
.coach-body {
  padding: 1.5rem;
  display: flex;
  flex-direction: column;
  gap: 1rem;
}
.coach-header {
  display: flex;
  align-items: flex-start;
  justify-content: space-between;
  gap: 1rem;
}
.coach-header h3 {
  font-size: 18px;
  font-weight: 600;
  color: #0d1f3c;
  margin: 0 0 4px;
}
.coach-role {
  font-size: 12px;
  color: #5a6a7a;
}
.coach-badge {
  background: #e8f0fb;
  color: #1455A4;
  font-size: 11px;
  font-weight: 600;
  padding: 4px 10px;
  border-radius: 20px;
  white-space: nowrap;
  flex-shrink: 0;
}
.coach-achievements {
  list-style: none;
  padding: 0;
  margin: 0;
  display: flex;
  flex-direction: column;
  gap: 6px;
}
.coach-achievements li {
  font-size: 13px;
  color: #5a6a7a;
  padding-left: 16px;
  position: relative;
  line-height: 1.5;
}
.coach-achievements li::before {
  content: '→';
  position: absolute;
  left: 0;
  color: #1455A4;
  font-size: 12px;
}

/* PRATIQUES */
.pratiques-grid {
  display: grid;
  grid-template-columns: repeat(4, 1fr);
  gap: 20px;
  margin-top: 2.5rem;
}
.pratique-card {
  background: #fff;
  border: 0.5px solid #e4eaf2;
  border-radius: 14px;
  padding: 1.75rem 1.5rem;
  box-shadow: 0 4px 16px rgba(10,30,70,0.06);
  transition: transform 0.2s ease, box-shadow 0.2s ease;
}
.pratique-card:hover {
  transform: translateY(-3px);
  box-shadow: 0 10px 28px rgba(10,30,70,0.1);
}
.pratique-icon {
  font-size: 28px;
  display: block;
  margin-bottom: 0.75rem;
}
.pratique-card h3 {
  font-size: 16px;
  font-weight: 600;
  color: #0d1f3c;
  margin-bottom: 8px;
}
.pratique-card p {
  font-size: 13px;
  color: #5a6a7a;
  line-height: 1.6;
}

/* CTA */
.cta-section {
  background: linear-gradient(135deg, #0a1f4e 0%, #1455A4 100%);
  padding: 5rem 2.5rem;
  text-align: center;
}
.cta-inner {
  max-width: 600px;
  margin: 0 auto;
}
.cta-inner h2 {
  font-family: 'Barlow Condensed', sans-serif;
  font-size: 48px;
  font-weight: 700;
  color: #fff;
  text-transform: uppercase;
  letter-spacing: 1px;
  margin-bottom: 1rem;
}
.cta-inner p {
  font-size: 16px;
  color: rgba(255,255,255,0.75);
  line-height: 1.7;
  margin-bottom: 2rem;
}
.cta-btns {
  display: flex;
  gap: 12px;
  justify-content: center;
}
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
</style>