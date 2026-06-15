<script setup>
definePageMeta({ layout: 'default' })

useSeoMeta({
  title: 'Open de Marseille — ASANDTT',
  description: 'Le 29ème Open National de Marseille aura lieu dimanche 30 août 2026. Inscriptions et règlement.'
})
</script>

<template>
  <div>
    <!-- HERO -->
    <section class="hero">
      <div class="hero-overlay" />
      <img
        src="/images/open-marseille.jpg"
        alt="Open de Marseille"
        class="hero-bg"
      >
      <div class="hero-content">
        <h1>Open de<br><strong>Marseille</strong></h1>
        <p>Le rendez-vous annuel du tennis de table marseillais. Une journée de compétition et de convivialité ouverte à tous les joueurs classés.</p>
        <div class="hero-date">
          <svg
            viewBox="0 0 24 24"
            fill="none"
            stroke="currentColor"
            stroke-width="1.5"
          ><rect
            x="3"
            y="4"
            width="18"
            height="18"
            rx="2"
          /><line
            x1="16"
            y1="2"
            x2="16"
            y2="6"
          /><line
            x1="8"
            y1="2"
            x2="8"
            y2="6"
          /><line
            x1="3"
            y1="10"
            x2="21"
            y2="10"
          /></svg>
          <span>Dimanche 30 août 2026</span>
        </div>
      </div>
    </section>

    <!-- REMERCIEMENTS + INFOS -->
    <section class="section section-white">
      <div class="section-inner main-grid">
        <div class="main-text">
          <h2>Merci pour le 28ème Open !</h2>
          <p>Un immense merci à tous pour votre présence lors du <strong>28ème Open National de Marseille</strong> qui a eu lieu dimanche 31 août 2025 !</p>
          <p>Un immense <strong>MERCI</strong> à la ville de Marseille, à la région SUD et au département des Bouches-du-Rhône pour leur soutien — sans vous, l'organisation de cet Open serait impossible.</p>
          <p>Nous espérons vous retrouver le <strong>30 août 2026</strong> pour faire de cette journée une belle fête du ping !</p>

          <div class="social-invite">
            <p>Suivez-nous sur les réseaux pour les dernières infos sur l'Open :</p>
            <div class="social-btns">
              <a
                href="https://www.facebook.com/p/ASAND-Marseille-Tennis-de-Table-100029105544587/?locale=fr_FR"
                target="_blank"
                class="soc-btn facebook"
              >
                <svg
                  viewBox="0 0 24 24"
                  fill="currentColor"
                  width="16"
                  height="16"
                ><path d="M18 2h-3a5 5 0 0 0-5 5v3H7v4h3v8h4v-8h3l1-4h-4V7a1 1 0 0 1 1-1h3z" /></svg>
                Facebook
              </a>
              <a
                href="https://www.instagram.com/asandmarseille/"
                target="_blank"
                class="soc-btn instagram"
              >
                <svg
                  viewBox="0 0 24 24"
                  fill="none"
                  stroke="currentColor"
                  stroke-width="1.8"
                  width="16"
                  height="16"
                ><rect
                  x="2"
                  y="2"
                  width="20"
                  height="20"
                  rx="5"
                /><circle
                  cx="12"
                  cy="12"
                  r="4"
                /><circle
                  cx="17.5"
                  cy="6.5"
                  r="1"
                  fill="currentColor"
                  stroke="none"
                /></svg>
                Instagram
              </a>
              <a
                href="https://www.tiktok.com/@asand.marseille"
                target="_blank"
                class="soc-btn tiktok"
              >
                <svg
                  viewBox="0 0 24 24"
                  fill="currentColor"
                  width="16"
                  height="16"
                ><path d="M19.59 6.69a4.83 4.83 0 0 1-3.77-4.25V2h-3.45v13.67a2.89 2.89 0 0 1-2.88 2.5 2.89 2.89 0 0 1-2.89-2.89 2.89 2.89 0 0 1 2.89-2.89c.28 0 .54.04.79.1V9.01a6.33 6.33 0 0 0-.79-.05 6.34 6.34 0 0 0-6.34 6.34 6.34 6.34 0 0 0 6.34 6.34 6.34 6.34 0 0 0 6.33-6.34V8.69a8.18 8.18 0 0 0 4.78 1.52V6.75a4.85 4.85 0 0 1-1.01-.06z" /></svg>
                TikTok
              </a>
            </div>
          </div>
        </div>

        <div class="main-side">
          <!-- INSCRIPTIONS -->
          <div class="info-block inscriptions">
            <div class="info-block-header">
              <div class="info-block-icon">
                <svg
                  viewBox="0 0 24 24"
                  fill="none"
                  stroke="currentColor"
                  stroke-width="1.5"
                ><path d="M17 21v-2a4 4 0 0 0-4-4H5a4 4 0 0 0-4 4v2" /><circle
                  cx="9"
                  cy="7"
                  r="4"
                /><path d="M23 21v-2a4 4 0 0 0-3-3.87" /><path d="M16 3.13a4 4 0 0 1 0 7.75" /></svg>
              </div>
              <div>
                <h3>Inscriptions 2026</h3>
              </div>
            </div>
            <p>Les inscriptions pour l'Open de Marseille 2026 ne sont pas encore ouvertes. Revenez bientôt ou suivez-nous sur les réseaux pour être informé dès l'ouverture.</p>
            <button
              class="btn-disabled"
              disabled
            >
              <svg
                viewBox="0 0 24 24"
                fill="none"
                stroke="currentColor"
                stroke-width="1.5"
                width="16"
                height="16"
              ><path d="M17 21v-2a4 4 0 0 0-4-4H5a4 4 0 0 0-4 4v2" /><circle
                cx="9"
                cy="7"
                r="4"
              /></svg>
              Inscription au tournoi annuel
            </button>
          </div>

          <!-- RÈGLEMENT -->
          <div class="info-block reglement">
            <div class="info-block-header">
              <div class="info-block-icon">
                <svg
                  viewBox="0 0 24 24"
                  fill="none"
                  stroke="currentColor"
                  stroke-width="1.5"
                ><path d="M14 2H6a2 2 0 0 0-2 2v16a2 2 0 0 0 2 2h12a2 2 0 0 0 2-2V8z" /><polyline points="14 2 14 8 20 8" /><line
                  x1="16"
                  y1="13"
                  x2="8"
                  y2="13"
                /><line
                  x1="16"
                  y1="17"
                  x2="8"
                  y2="17"
                /></svg>
              </div>
              <div>
                <h3>Règlement 2026</h3>
              </div>
            </div>
            <p>Le règlement de l'Open de Marseille 2026 sera communiqué quelques semaines avant le tournoi.</p>
            <div class="reglement-btns">
              <button
                class="btn-disabled"
                disabled
              >
                <svg
                  viewBox="0 0 24 24"
                  fill="none"
                  stroke="currentColor"
                  stroke-width="1.5"
                  width="16"
                  height="16"
                ><path d="M14 2H6a2 2 0 0 0-2 2v16a2 2 0 0 0 2 2h12a2 2 0 0 0 2-2V8z" /><polyline points="14 2 14 8 20 8" /></svg>
                Règlement sportif
              </button>
              <button
                class="btn-disabled"
                disabled
              >
                <svg
                  viewBox="0 0 24 24"
                  fill="none"
                  stroke="currentColor"
                  stroke-width="1.5"
                  width="16"
                  height="16"
                ><path d="M14 2H6a2 2 0 0 0-2 2v16a2 2 0 0 0 2 2h12a2 2 0 0 0 2-2V8z" /><polyline points="14 2 14 8 20 8" /></svg>
                Règlement général
              </button>
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
  background: linear-gradient(to right, rgba(10,30,70,0.93) 0%, rgba(10,30,70,0.7) 55%, rgba(10,30,70,0.2) 100%);
  z-index: 1;
}
.hero-content {
  position: relative;
  z-index: 2;
  padding: 4rem 5rem;
  max-width: 640px;
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
  font-size: 72px;
  font-weight: 400;
  color: #fff;
  line-height: 1.0;
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
  margin-bottom: 1.5rem;
}
.hero-date {
  display: inline-flex;
  align-items: center;
  gap: 8px;
  background: #1455A4;
  color: #fff;
  padding: 10px 20px;
  border-radius: 8px;
  font-size: 15px;
  font-weight: 600;
}
.hero-date svg { width: 18px; height: 18px; }

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

/* MAIN GRID */
.main-grid {
  display: grid;
  grid-template-columns: 1fr 400px;
  gap: 3.5rem;
  align-items: start;
}
.main-text p {
  font-size: 15px;
  color: #5a6a7a;
  line-height: 1.75;
  margin-bottom: 1rem;
}
.main-text strong { color: #0d1f3c; }

/* SOCIALS */
.social-invite {
  margin-top: 2rem;
  padding-top: 1.5rem;
  border-top: 0.5px solid #e4eaf2;
}
.social-invite p {
  font-size: 14px;
  color: #5a6a7a;
  margin-bottom: 1rem !important;
}
.social-btns { display: flex; gap: 10px; flex-wrap: wrap; }
.soc-btn {
  display: inline-flex;
  align-items: center;
  gap: 7px;
  padding: 9px 16px;
  border-radius: 8px;
  font-size: 13px;
  font-weight: 600;
  text-decoration: none;
  transition: opacity 0.15s ease;
}
.soc-btn:hover { opacity: 0.85; }
.facebook { background: #1877F2; color: #fff; }
.instagram { background: linear-gradient(135deg, #f09433, #e6683c, #dc2743, #cc2366, #bc1888); color: #fff; }
.tiktok { background: #010101; color: #fff; }

/* INFO BLOCKS */
.main-side { display: flex; flex-direction: column; gap: 1.5rem; }
.info-block {
  background: #fff;
  border: 0.5px solid #e4eaf2;
  border-radius: 16px;
  padding: 1.5rem;
  box-shadow: 0 4px 16px rgba(10,30,70,0.06);
}
.info-block-header {
  display: flex;
  align-items: flex-start;
  gap: 12px;
  margin-bottom: 1rem;
}
.info-block-icon {
  width: 40px;
  height: 40px;
  background: #e8f0fb;
  border-radius: 10px;
  display: flex;
  align-items: center;
  justify-content: center;
  flex-shrink: 0;
}
.info-block-icon svg { width: 20px; height: 20px; color: #1455A4; }
.info-block h3 {
  font-size: 16px;
  font-weight: 600;
  color: #0d1f3c;
  margin: 0 0 5px;
}
.info-block p {
  font-size: 13px;
  color: #5a6a7a;
  line-height: 1.6;
  margin-bottom: 1.25rem;
}
.status-badge {
  font-size: 11px;
  font-weight: 600;
  padding: 3px 10px;
  border-radius: 20px;
  display: inline-block;
}
.status-badge.closed {
  background: #fef3c7;
  color: #92400e;
}
.status-badge.pending {
  background: #e8f0fb;
  color: #1455A4;
}
.btn-disabled {
  display: inline-flex;
  align-items: center;
  gap: 8px;
  background: #e4eaf2;
  color: #8899aa;
  border: none;
  padding: 10px 18px;
  border-radius: 8px;
  font-size: 13px;
  font-weight: 500;
  cursor: not-allowed;
  width: 100%;
  justify-content: center;
  font-family: inherit;
}
.reglement-btns { display: flex; flex-direction: column; gap: 8px; }
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
  .hero-content h1 { font-size: 48px; }
  .hero-content p { font-size: 15px; max-width: 100%; }
  .hero-date { font-size: 13px; padding: 8px 14px; }

  /* SECTIONS */
  .section { padding: 3rem 1.25rem; }
  .section h2 { font-size: 24px; }

  /* MAIN GRID */
  .main-grid {
    grid-template-columns: 1fr;
    gap: 2rem;
  }

  /* SOCIALS */
  .social-btns {
    flex-direction: column;
    gap: 8px;
  }
  .soc-btn { width: 100%; justify-content: center; }

  /* CTA */
  .cta-section { padding: 3rem 1.5rem; }
  .cta-inner h2 { font-size: 32px; }
  .cta-inner p { font-size: 14px; }
}
</style>
