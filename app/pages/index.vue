<script setup>
definePageMeta({
  layout: 'default'
})

useSeoMeta({
  title: 'ASANDTT Marseille — Tennis de table',
  description: 'Club de tennis de table à Marseille. Tous niveaux, tous âges. Loisir et compétition.',
})
</script>

<template>
  <div>

    <!-- HERO -->
    <section class="hero">
      <div class="hero-content">
        <div class="hero-badge">
          <span>Club affilié FFTT · Marseille</span>
        </div>
        <h1>Plus qu'un club,<br/><em>une famille</em></h1>
        <p>Rejoignez l'ASANDTT — 20 tables, tous niveaux, tous âges. Du loisir à la compétition, dans un grand gymnase au cœur de Marseille.</p>
        <div class="hero-btns">
          <NuxtLink to="/inscription" class="btn-primary">Nous rejoindre</NuxtLink>
          <NuxtLink to="/club" class="btn-outline">Découvrir le club</NuxtLink>
        </div>
      </div>
<div class="hero-img">
  <ClubPhoto height="480px" alt="Gymnase ASANDTT Marseille" />
</div>
    </section>

    <!-- STATS -->
    <div class="stats-row">
      <div class="stat">
        <span class="stat-n">20</span>
        <span class="stat-l">Tables</span>
      </div>
      <div class="stat">
        <span class="stat-n">150+</span>
        <span class="stat-l">Licenciés</span>
      </div>
      <div class="stat">
        <span class="stat-n">5</span>
        <span class="stat-l">Équipes</span>
      </div>
      <div class="stat">
        <span class="stat-n">40+</span>
        <span class="stat-l">Ans d'histoire</span>
      </div>
    </div>

    <!-- LE CLUB -->
    <section class="section section-white">
      <div class="section-inner">
        <span class="section-tag">Le club</span>
        <h2>Pratiquer, progresser, partager</h2>
        <p class="section-intro">Une structure conviviale pour découvrir ou se perfectionner au tennis de table. Débutant ou compétiteur, nous vous accueillons dans une ambiance dynamique.</p>
        <div class="cards-grid">
          <div class="card">
            <div class="card-icon">🏆</div>
            <h3>Compétitions</h3>
            <p>Championnats par équipes et individuels pour tous les niveaux.</p>
            <NuxtLink to="/competitions" class="card-link">En savoir plus →</NuxtLink>
          </div>
          <div class="card">
            <div class="card-icon">📅</div>
            <h3>Entraînements</h3>
            <p>Plusieurs créneaux par semaine, du lundi au vendredi.</p>
            <NuxtLink to="/inscription" class="card-link">Voir le planning →</NuxtLink>
          </div>
          <div class="card">
            <div class="card-icon">⭐</div>
            <h3>Open de Marseille</h3>
            <p>Notre tournoi annuel, ouvert à tous les joueurs classés.</p>
            <NuxtLink to="/open-marseille" class="card-link">En savoir plus →</NuxtLink>
          </div>
          <div class="card">
            <div class="card-icon">❤️</div>
            <h3>Sport santé</h3>
            <p>Le ping accessible à tous, y compris les seniors et débutants.</p>
            <NuxtLink to="/club" class="card-link">En savoir plus →</NuxtLink>
          </div>
        </div>
      </div>
    </section>

    <!-- ACTUALITÉS -->
    <section class="section section-grey">
      <div class="section-inner">
        <span class="section-tag">Actualités</span>
        <h2>Les dernières nouvelles du club</h2>
        <div class="news-grid">
          <div class="news-card">
            <div class="news-img-placeholder"></div>
            <div class="news-body">
              <span class="news-tag">Vie du club</span>
              <p class="news-title">Inscriptions ouvertes toute l'année !</p>
              <span class="news-date">11 décembre 2024</span>
            </div>
          </div>
          <div class="news-card">
            <div class="news-img-placeholder"></div>
            <div class="news-body">
              <span class="news-tag">Réseaux sociaux</span>
              <p class="news-title">Suivez-nous sur Facebook et Instagram</p>
              <span class="news-date">28 décembre 2021</span>
            </div>
          </div>
          <div class="news-card">
            <div class="news-img-placeholder"></div>
            <div class="news-body">
              <span class="news-tag">Compétition</span>
              <p class="news-title">Résultats de la dernière journée de championnat</p>
              <span class="news-date">À venir</span>
            </div>
          </div>
        </div>
      </div>
    </section>

    <!-- AGENDA -->
    <section class="section section-white">
      <div class="section-inner">
        <span class="section-tag">Agenda</span>
        <h2>Prochaines rencontres</h2>
        <div class="agenda-grid">
          <div class="agenda-item">
            <div class="agenda-date">
              <span class="day">30</span>
              <span class="month">Mai</span>
            </div>
            <div class="agenda-info">
              <h4>Championnat — 6ème journée</h4>
              <p>Gymnase Artaud, Marseille</p>
            </div>
          </div>
          <div class="agenda-item">
            <div class="agenda-date">
              <span class="day">06</span>
              <span class="month">Juin</span>
            </div>
            <div class="agenda-info">
              <h4>Championnat — 7ème journée</h4>
              <p>Gymnase Artaud, Marseille</p>
            </div>
          </div>
        </div>
      </div>
    </section>

  </div>
</template>

<style scoped>
/* HERO */
.hero {
  background: #0d1f3c;
  display: flex;
  align-items: center;
  min-height: 480px;
  position: relative;
  overflow: hidden;
}
.hero-content {
  flex: 1;
  padding: 4rem 2.5rem;
  max-width: 600px;
  z-index: 1;
}
.hero-badge {
  display: inline-block;
  background: rgba(255,255,255,0.08);
  border: 0.5px solid rgba(255,255,255,0.15);
  color: #9bbfdf;
  font-size: 12px;
  letter-spacing: 1.5px;
  text-transform: uppercase;
  padding: 5px 13px;
  border-radius: 20px;
  margin-bottom: 1.5rem;
}
.hero-content h1 {
  font-size: 44px;
  font-weight: 500;
  color: #fff;
  line-height: 1.15;
  margin-bottom: 1rem;
  letter-spacing: -0.5px;
}
.hero-content h1 em {
  color: #5BA4E5;
  font-style: normal;
}
.hero-content p {
  font-size: 16px;
  color: #8daec9;
  line-height: 1.7;
  margin-bottom: 2rem;
  max-width: 460px;
}
.hero-btns { display: flex; gap: 10px; flex-wrap: wrap; }
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

/* STATS */
.stats-row {
  background: #fff;
  border-bottom: 0.5px solid #e8edf3;
  display: flex;
  justify-content: center;
}
.stat {
  padding: 1.4rem 3rem;
  text-align: center;
  border-right: 0.5px solid #e8edf3;
}
.stat:last-child { border-right: none; }
.stat-n {
  font-size: 30px;
  font-weight: 500;
  color: #1455A4;
  display: block;
}
.stat-l {
  font-size: 11px;
  color: #8899aa;
  letter-spacing: 0.8px;
  text-transform: uppercase;
  margin-top: 2px;
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
  color: #0d1f3c;
  margin-bottom: 0.75rem;
  letter-spacing: -0.3px;
}
.section-intro {
  font-size: 16px;
  color: #5a6a7a;
  line-height: 1.7;
  max-width: 560px;
}

/* CARDS */
.cards-grid {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(220px, 1fr));
  gap: 16px;
  margin-top: 2.5rem;
}
.card {
  background: #fff;
  border: 0.5px solid #e4eaf2;
  border-radius: 14px;
  padding: 1.5rem;
}
.card-icon { font-size: 24px; margin-bottom: 1rem; }
.card h3 { font-size: 15px; font-weight: 500; color: #0d1f3c; margin-bottom: 6px; }
.card p { font-size: 13px; color: #5a6a7a; line-height: 1.6; }
.card-link {
  font-size: 13px;
  color: #1455A4;
  text-decoration: none;
  margin-top: 10px;
  display: inline-block;
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
  height: 140px;
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
</style>