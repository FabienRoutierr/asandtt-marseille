<script setup>
definePageMeta({ layout: 'default' })

useSeoMeta({
  title: 'Compétitions — ASANDTT Marseille',
  description: 'Le club numéro 1 de Marseille en compétition de tennis de table, du niveau départemental au national.',
})

const topPlayers = [
  { rank: 1, name: 'Sébastien MALET', detail: 'N° 1 de Marseille · Numéroté FFTT depuis 25 ans · Formé à l\'ASAND' },
  { rank: 2, name: 'Michel FRANQUEBALME', detail: 'N° 2 de Marseille · Entraîneur · Numéroté FFTT depuis +25 ans' },
  { rank: 3, name: 'Steve WOUDSTRA', detail: 'N° 3 de Marseille · Classé 20 · Formé à l\'ASAND' },
  { rank: 4, name: 'Lucas ROUTIER', detail: 'N° 4 de Marseille · Classé 19 · Formé à l\'ASAND' },
  { rank: 5, name: 'Célian ARMAND', detail: 'N° 5 de Marseille · Classé 19' },
  { rank: 6, name: 'Pierre MONDON', detail: 'N° 6 de Marseille · Classé 18' },
  { rank: 7, name: 'Kelvin BEVILACQUA', detail: 'N° 7 de Marseille · Classé 17 · Formé à l\'ASAND' },
  { rank: 8, name: 'Alexandre ROUTIER', detail: 'Classé 16 · Formé à l\'ASAND' },
  { rank: 9, name: 'Jean MOUTIN', detail: 'Classé 15 (ancien 18) · Formé à l\'ASAND' },
]
</script>

<template>
  <div>

    <!-- HERO -->
    <section class="hero">
      <div class="hero-overlay"></div>
      <img src="/images/equipe_asand.jpeg" alt="Équipe 1 ASANDTT — National 3" class="hero-bg" />
      <div class="hero-content">
        <h1>La compétition<br/><strong>à tous les niveaux</strong></h1>
        <p>Le seul club de Marseille qui évolue au niveau national, avec 8 équipes du départemental au national.</p>
      </div>
    </section>

    <!-- INTRO -->
    <section class="section section-white">
      <div class="section-inner intro-grid">
        <div class="intro-text">
          <h2>ASAND, meilleur club de Marseille</h2>
          <p>L'ASAND est le club numéro 1 de la ville de Marseille. Nous avons la chance d'avoir de nombreux compétiteurs de tous les niveaux au sein du club, et nous sommes fiers d'avoir les joueurs les mieux classés de la ville de Marseille — tous clubs confondus — dans les catégories jeunes et adultes.</p>
          <p>Nous sommes le seul club de la ville de Marseille qui évolue au niveau national. Nous pratiquons aussi la compétition au niveau départemental et régional, en individuel et en équipes.</p>
        </div>
        <div class="intro-stats">
          <div class="intro-stat">
            <span class="intro-stat-n">8</span>
            <span class="intro-stat-l">Équipes engagées</span>
          </div>
          <div class="intro-stat">
            <span class="intro-stat-n">N3</span>
            <span class="intro-stat-l">Niveau national</span>
          </div>
          <div class="intro-stat">
            <span class="intro-stat-n">N°1</span>
            <span class="intro-stat-l">Club de Marseille</span>
          </div>
        </div>
      </div>
    </section>

    <!-- JOUEURS -->
    <section class="section section-grey">
      <div class="section-inner">
        <h2>Les mieux classés de Marseille</h2>
        <p class="section-intro">Tous clubs confondus, l'ASAND domine le classement marseillais avec les meilleurs joueurs de la ville.</p>
        <div class="players-grid">
          <div v-for="player in topPlayers" :key="player.rank" class="player-card">
            <div class="player-rank">#{{ player.rank }}</div>
            <div class="player-info">
              <span class="player-name">{{ player.name }}</span>
              <span class="player-detail">{{ player.detail }}</span>
            </div>
          </div>
        </div>
      </div>
    </section>

    <!-- JEUNES -->
    <section class="section section-white">
      <div class="section-inner jeunes-grid">
        <div class="jeunes-img">
          <img src="/images/photo_club.jpeg" alt="Jeunes joueurs ASANDTT" />
        </div>
        <div class="jeunes-text">
          <h2>Notre priorité : les jeunes talents</h2>
          <p>Les jeunes joueurs sont notre priorité au club de l'ASAND. Ils sont progressivement intégrés dans nos équipes avec les adultes pour accélérer leur progression.</p>
          <div class="jeune-highlight">
            <div class="jeune-badge">N°1 U19 Marseille</div>
            <div class="jeune-content">
              <strong>Lucas ROUTIER</strong> (17 ans) est n°1 de la ville de Marseille tous clubs confondus chez les moins de 19 ans. Il évolue au niveau national en individuel et avec notre équipe fanion.
            </div>
          </div>
          <div class="jeune-highlight">
            <div class="jeune-badge">N°1 U15 Marseille</div>
            <div class="jeune-content">
              <strong>Raphael LAZARD</strong> (14 ans) vient de nous rejoindre. Il est également n°1 de la ville de Marseille tous clubs confondus chez les moins de 15 ans.
            </div>
          </div>
          <p class="jeunes-coaching">Nos jeunes sont suivis lors des différentes compétitions par notre entraîneur <strong>Michel FRANQUEBALME</strong>, et par nos joueurs expérimentés qui viennent régulièrement aider au coaching.</p>
        </div>
      </div>
    </section>

  </div>
</template>

<style scoped>
/* HERO */
.hero {
  position: relative;
  min-height: 720px;
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
  object-position: center top;
}
.hero-overlay {
  position: absolute;
  inset: 0;
  background: linear-gradient(to right, rgba(10,30,70,0.90) 0%, rgba(10,30,70,0.60) 55%, rgba(10,30,70,0.15) 100%);
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
  margin-bottom: 0;
}

/* INTRO GRID */
.intro-grid {
  display: grid;
  grid-template-columns: 1fr 300px;
  gap: 4rem;
  align-items: center;
}
.intro-text p {
  font-size: 15px;
  color: #5a6a7a;
  line-height: 1.75;
  margin-bottom: 1rem;
}
.intro-stats {
  display: flex;
  flex-direction: column;
  gap: 1.5rem;
}
.intro-stat {
  background: linear-gradient(135deg, #1949b0 0%, #3074c7 100%);
  border-radius: 16px;
  padding: 1.5rem;
  text-align: center;
}
.intro-stat-n {
  font-family: 'Barlow Condensed', sans-serif;
  font-size: 48px;
  font-weight: 700;
  color: #fff;
  display: block;
  line-height: 1;
}
.intro-stat-l {
  font-size: 12px;
  color: rgba(255,255,255,0.6);
  letter-spacing: 1.5px;
  text-transform: uppercase;
  margin-top: 6px;
  display: block;
}

/* PLAYERS */
.players-grid {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(320px, 1fr));
  gap: 12px;
  margin-top: 2.5rem;
}
.player-card {
  background: #fff;
  border: 0.5px solid #e4eaf2;
  border-radius: 12px;
  padding: 1rem 1.25rem;
  display: flex;
  align-items: center;
  gap: 1rem;
  transition: box-shadow 0.2s ease, transform 0.2s ease;
}
.player-card:hover {
  box-shadow: 0 6px 20px rgba(10,30,70,0.08);
  transform: translateY(-2px);
}
.player-rank {
  font-family: 'Barlow Condensed', sans-serif;
  font-size: 28px;
  font-weight: 700;
  color: #1455A4;
  min-width: 48px;
  text-align: center;
  opacity: 0.7;
}
.player-info {
  display: flex;
  flex-direction: column;
  gap: 3px;
}
.player-name {
  font-size: 15px;
  font-weight: 600;
  color: #0d1f3c;
}
.player-detail {
  font-size: 12px;
  color: #8899aa;
  letter-spacing: 0.2px;
}

/* JEUNES */
.jeunes-grid {
  display: grid;
  grid-template-columns: 1fr 1fr;
  gap: 4rem;
  align-items: start;
}
.jeunes-img {
  border-radius: 16px;
  overflow: hidden;
  height: 500px;
}
.jeunes-img img {
  width: 100%;
  height: 100%;
  object-fit: cover;
}
.jeunes-text p {
  font-size: 15px;
  color: #5a6a7a;
  line-height: 1.75;
  margin-bottom: 1.25rem;
}
.jeune-highlight {
  background: #f0f5fb;
  border-left: 3px solid #1455A4;
  border-radius: 0 12px 12px 0;
  padding: 1rem 1.25rem;
  margin-bottom: 1rem;
  display: flex;
  flex-direction: column;
  gap: 6px;
}
.jeune-badge {
  font-size: 11px;
  font-weight: 600;
  color: #1455A4;
  letter-spacing: 0.5px;
  text-transform: uppercase;
}
.jeune-content {
  font-size: 14px;
  color: #3d4f63;
  line-height: 1.6;
}
.jeunes-coaching {
  font-size: 14px;
  color: #5a6a7a;
  line-height: 1.7;
  font-style: italic;
  border-top: 0.5px solid #e4eaf2;
  padding-top: 1rem;
  margin-top: 0.5rem;
}

/* ============ RESPONSIVE MOBILE ============ */
@media (max-width: 900px) {

  /* HERO */
  .hero {
    min-height: 420px;
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
  .hero-content h1 { font-size: 38px; }
  .hero-content p { font-size: 15px; max-width: 100%; }

  /* SECTIONS */
  .section { padding: 3rem 1.25rem; }
  .section h2 { font-size: 24px; }
  .section-intro { font-size: 14px; }

  /* INTRO GRID */
  .intro-grid {
    grid-template-columns: 1fr;
    gap: 2rem;
  }
  .intro-stats {
    flex-direction: row;
    gap: 12px;
  }
  .intro-stat {
    flex: 1;
    padding: 1rem 0.75rem;
  }
  .intro-stat-n { font-size: 32px; }
  .intro-stat-l { font-size: 10px; letter-spacing: 0.5px; }

  /* PLAYERS */
  .players-grid {
    grid-template-columns: 1fr;
    gap: 8px;
    margin-top: 1.5rem;
  }
  .player-rank { font-size: 22px; min-width: 36px; }
  .player-name { font-size: 14px; }

  /* JEUNES */
  .jeunes-grid {
    grid-template-columns: 1fr;
    gap: 2rem;
  }
  .jeunes-img {
    height: 240px;
  }
}
</style>