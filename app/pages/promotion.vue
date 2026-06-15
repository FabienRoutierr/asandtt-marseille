<script setup>
definePageMeta({ layout: 'default' })

useSeoMeta({
  title: 'Promotion — ASANDTT Marseille',
  description: 'Téléchargez et partagez les affiches et flyers du club ASANDTT Marseille.',
})
</script>

<template>
  <div>

    <!-- CONTENU -->
    <section class="section section-white">
      <div class="section-inner">
        <div class="promo-grid">

          <!-- TEXTE -->
          <div class="promo-text">
            <h2>Faites la publicité du club !</h2>
            <p>Nous avons le plaisir de vous partager notre affiche. N'hésitez pas à faire la publicité du club autour de vous grâce aux différents flyers et affiches disponibles à la salle.</p>
            <div class="promo-info">
              <div class="promo-info-item">
                <span>N’hésitez pas à nous suivre sur les réseaux sociaux pour être informé de toutes les actualités du club :</span>
              </div>
            </div>
<div class="promo-btns">
  <a href="https://www.facebook.com/p/ASAND-Marseille-Tennis-de-Table-100029105544587/?locale=fr_FR" target="_blank" class="social-btn facebook" aria-label="Facebook">
    <svg viewBox="0 0 24 24" fill="currentColor"><path d="M18 2h-3a5 5 0 0 0-5 5v3H7v4h3v8h4v-8h3l1-4h-4V7a1 1 0 0 1 1-1h3z"/></svg>
    <span>Facebook</span>
  </a>
  <a href="https://www.instagram.com/asandmarseille/" target="_blank" class="social-btn instagram" aria-label="Instagram">
    <svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="1.8"><rect x="2" y="2" width="20" height="20" rx="5"/><circle cx="12" cy="12" r="4"/><circle cx="17.5" cy="6.5" r="1" fill="currentColor" stroke="none"/></svg>
    <span>Instagram</span>
  </a>
  <a href="https://www.tiktok.com/@asand.marseille" target="_blank" class="social-btn tiktok" aria-label="TikTok">
    <svg viewBox="0 0 24 24" fill="currentColor"><path d="M19.59 6.69a4.83 4.83 0 0 1-3.77-4.25V2h-3.45v13.67a2.89 2.89 0 0 1-2.88 2.5 2.89 2.89 0 0 1-2.89-2.89 2.89 2.89 0 0 1 2.89-2.89c.28 0 .54.04.79.1V9.01a6.33 6.33 0 0 0-.79-.05 6.34 6.34 0 0 0-6.34 6.34 6.34 6.34 0 0 0 6.34 6.34 6.34 6.34 0 0 0 6.33-6.34V8.69a8.18 8.18 0 0 0 4.78 1.52V6.75a4.85 4.85 0 0 1-1.01-.06z"/></svg>
    <span>TikTok</span>
  </a>
</div>
          </div>

          <!-- AFFICHE -->
          <div class="promo-poster">
            <img src="/images/affiche_asand.jpg" alt="Affiche ASANDTT Marseille" />
          </div>

        </div>
      </div>
    </section>

  </div>
</template>

<style scoped>
.hero {
  position: relative;
  min-height: 380px;
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

.section { padding: 5rem 2.5rem; }
.section-white { background: #fff; }
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

.promo-grid {
  display: grid;
  grid-template-columns: 1fr 420px;
  gap: 5rem;
  align-items: center;
}
.promo-text p {
  font-size: 15px;
  color: #5a6a7a;
  line-height: 1.75;
  margin-bottom: 2rem;
}
.promo-info {
  display: flex;
  flex-direction: column;
  gap: 14px;
  margin-bottom: 2rem;
}
.promo-info-item {
  display: flex;
  align-items: flex-start;
  gap: 12px;
}
.promo-info-item svg {
  width: 18px;
  height: 18px;
  color: #1455A4;
  flex-shrink: 0;
  margin-top: 2px;
}
.promo-info-item span {
  font-size: 14px;
  color: #5a6a7a;
  line-height: 1.5;
}
.promo-btns {
  display: flex;
  gap: 12px;
  flex-wrap: wrap;
}
.btn-primary {
  background: #1455A4;
  color: #fff;
  padding: 12px 28px;
  border-radius: 8px;
  font-size: 14px;
  font-weight: 600;
  text-decoration: none;
  transition: background 0.15s ease;
}
.btn-primary:hover { background: #0f3f85; }

.promo-poster {
  border-radius: 16px;
  overflow: hidden;
  box-shadow: 0 20px 60px rgba(10,30,70,0.15);
}
.promo-poster img {
  width: 100%;
  height: auto;
  display: block;
}

.social-btn {
  display: flex;
  align-items: center;
  gap: 8px;
  padding: 11px 20px;
  border-radius: 10px;
  font-size: 14px;
  font-weight: 600;
  text-decoration: none;
  transition: transform 0.15s ease, box-shadow 0.15s ease;
}
.social-btn:hover {
  transform: translateY(-2px);
  box-shadow: 0 6px 20px rgba(0,0,0,0.15);
}
.social-btn svg {
  width: 20px;
  height: 20px;
  flex-shrink: 0;
}
.facebook {
  background: #1877F2;
  color: #fff;
}
.instagram {
  background: linear-gradient(135deg, #f09433 0%, #e6683c 25%, #dc2743 50%, #cc2366 75%, #bc1888 100%);
  color: #fff;
}
.tiktok {
  background: #010101;
  color: #fff;
}
/* ============ RESPONSIVE MOBILE ============ */
@media (max-width: 900px) {

  /* SECTION */
  .section { padding: 3rem 1.25rem; }
  .section h2 { font-size: 24px; }

  /* PROMO GRID */
  .promo-grid {
    grid-template-columns: 1fr;
    gap: 2.5rem;
  }

  /* AFFICHE remontée au-dessus du texte */
  .promo-poster { order: -1; }

  /* BOUTONS SOCIAUX */
  .promo-btns {
    flex-direction: column;
    gap: 10px;
  }
  .social-btn { justify-content: center; width: 100%; }
}
</style>