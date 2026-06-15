<template>
  <footer class="footer">
    <div class="footer-grid">

      <!-- BRAND -->
      <div class="footer-brand">
        <NuxtLink to="/">
          <img src="/images/logo_asand3.png" alt="Logo ASANDTT" class="footer-logo" />
        </NuxtLink>
        <p class="brand-desc">Club affilié à la FFTT, ouvert à tous depuis plus de 40 ans. 20 tables, plusieurs créneaux hebdomadaires, loisir et compétition.</p>
        <div class="socials">
          <a href="https://www.facebook.com/p/ASAND-Marseille-Tennis-de-Table-100029105544587/?locale=fr_FR" target="_blank" class="soc" aria-label="Facebook">
            <svg width="16" height="16" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="1.8"><path d="M18 2h-3a5 5 0 0 0-5 5v3H7v4h3v8h4v-8h3l1-4h-4V7a1 1 0 0 1 1-1h3z"/></svg>
          </a>
          <a href="https://www.instagram.com/asandmarseille/" target="_blank" class="soc" aria-label="Instagram">
            <svg width="16" height="16" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="1.8"><rect x="2" y="2" width="20" height="20" rx="5"/><circle cx="12" cy="12" r="4"/><circle cx="17.5" cy="6.5" r="0.5" fill="currentColor"/></svg>
          </a>
          <a href="https://www.tiktok.com/@asand.marseille" target="_blank" class="soc" aria-label="TikTok">
            <svg width="16" height="16" viewBox="0 0 24 24" fill="currentColor"><path d="M19.59 6.69a4.83 4.83 0 0 1-3.77-4.25V2h-3.45v13.67a2.89 2.89 0 0 1-2.88 2.5 2.89 2.89 0 0 1-2.89-2.89 2.89 2.89 0 0 1 2.89-2.89c.28 0 .54.04.79.1V9.01a6.33 6.33 0 0 0-.79-.05 6.34 6.34 0 0 0-6.34 6.34 6.34 6.34 0 0 0 6.34 6.34 6.34 6.34 0 0 0 6.33-6.34V8.69a8.18 8.18 0 0 0 4.78 1.52V6.75a4.85 4.85 0 0 1-1.01-.06z"/></svg>
          </a>
        </div>
      </div>

      <!-- NAVIGATION -->
      <div class="footer-col">
        <div class="accent"></div>
        <h4>Navigation</h4>
        <ul>
          <li><NuxtLink to="/">Accueil</NuxtLink></li>
          <li><NuxtLink to="/association">L'association</NuxtLink></li>
          <li><NuxtLink to="/competitions">Compétitions</NuxtLink></li>
          <li><NuxtLink to="/open-marseille">Open de Marseille</NuxtLink></li>
          <li><NuxtLink to="/promotion">Promotion</NuxtLink></li>
          <li><NuxtLink to="/contact">Nous contacter</NuxtLink></li>
        </ul>
      </div>

      <!-- CONTACT -->
      <div class="footer-col">
        <div class="accent"></div>
        <h4>Contact</h4>
        <div class="contact-item">
          <svg width="15" height="15" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="1.8"><path d="M21 10c0 7-9 13-9 13s-9-6-9-13a9 9 0 0 1 18 0z"/><circle cx="12" cy="10" r="3"/></svg>
          <span>Gymnase Antonin Artaud<br/>25 chemin Notre Dame de Consolation<br/>13013 Marseille</span>
        </div>
        <div class="contact-item">
          <svg width="15" height="15" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="1.8"><circle cx="12" cy="12" r="10"/><polyline points="12 6 12 12 16 14"/></svg>
          <span>Lun – Ven : 17h30 – 21h</span>
        </div>
        <div class="contact-item">
          <svg width="15" height="15" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="1.8"><path d="M22 16.92v3a2 2 0 0 1-2.18 2 19.79 19.79 0 0 1-8.63-3.07A19.5 19.5 0 0 1 4.69 12a19.79 19.79 0 0 1-3.07-8.67A2 2 0 0 1 3.6 1.27h3a2 2 0 0 1 2 1.72c.127.96.361 1.903.7 2.81a2 2 0 0 1-.45 2.11L7.91 8.91a16 16 0 0 0 6 6l.95-.95a2 2 0 0 1 2.11-.45c.907.339 1.85.573 2.81.7A2 2 0 0 1 22 16.92z"/></svg>
          <span>04 91 78 80 00</span>
        </div>
        <div class="contact-item">
          <svg width="15" height="15" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="1.8"><path d="M4 4h16c1.1 0 2 .9 2 2v12c0 1.1-.9 2-2 2H4c-1.1 0-2-.9-2-2V6c0-1.1.9-2 2-2z"/><polyline points="22,6 12,13 2,6"/></svg>
          <span>contact@asandtt-marseille.fr</span>
        </div>
      </div>

    </div>

    <!-- LIGNE BAS -->
<div class="footer-bottom">
  <span>© {{ new Date().getFullYear() }} ASANDTT Marseille</span>
  <div class="footer-legal">
    <NuxtLink to="/mentions-legales">Mentions légales</NuxtLink>
    <span class="sep">·</span>
    <NuxtLink to="/confidentialite">Politique de confidentialité</NuxtLink>
  </div>
</div>
  </footer>
</template>

<script setup>
</script>

<style scoped>
.footer {
  background: #fff;
  border-top: 1px solid #e4eaf2;
  padding: 3.5rem 2.5rem 1.5rem;
}
.footer-grid {
  display: grid;
  grid-template-columns: 2fr 1fr 1fr;
  gap: 3rem;
  max-width: 1100px;
  margin: 0 auto;
}

/* BRAND */
.footer-logo {
  height: 130px;
  width: auto;
  object-fit: contain;
  display: block;
  margin-bottom: 2rem;
}
.brand-desc {
  font-size: 13px;
  color: #5a6a7a;
  line-height: 1.7;
  max-width: 280px;
  margin-top: 0.25rem;
}
.socials { display: flex; gap: 8px; margin-top: 1.2rem; }
.soc {
  width: 34px;
  height: 34px;
  border-radius: 8px;
  background: #f0f5fb;
  border: 0.5px solid #e4eaf2;
  display: flex;
  align-items: center;
  justify-content: center;
  color: #0e3471;
  text-decoration: none;
  transition: background 0.15s ease;
}
.soc:hover { background: #e8f0fb; color: #0f3f85; }

/* COLONNES */
.footer-col h4 {
  font-size: 14px;
  color: #0e3471;
  letter-spacing: 1.5px;
  text-transform: uppercase;
  margin-bottom: 1rem;
  font-weight: 700;
}
.accent {
  width: 32px;
  height: 2.5px;
  background: #3293d4;
  border-radius: 2px;
  margin-bottom: 0.9rem;
}
.footer-col ul { list-style: none; }
.footer-col ul li { margin-bottom: 8px; }
.footer-col ul li a {
  font-size: 13px;
  color: #5a6a7a;
  text-decoration: none;
  transition: color 0.15s ease;
}
.footer-col ul li a:hover { color: #0e3471; }

/* CONTACT */
.contact-item {
  display: flex;
  align-items: flex-start;
  gap: 8px;
  margin-bottom: 10px;
}
.contact-item svg { color: #3293d4; flex-shrink: 0; margin-top: 2px; }
.contact-item span { font-size: 13px; color: #5a6a7a; line-height: 1.5; }

/* LIGNE BAS */
.footer-bottom {
  max-width: 1100px;
  margin: 2rem auto 0;
  padding-top: 1.25rem;
  border-top: 0.5px solid #e4eaf2;
  font-size: 12px;
  color: #8899aa;
  display: flex;
  align-items: center;
  justify-content: space-between;
  flex-wrap: wrap;
  gap: 8px;
}
.footer-legal {
  display: flex;
  align-items: center;
  gap: 8px;
}
.footer-legal a {
  font-size: 12px;
  color: #8899aa;
  text-decoration: none;
  transition: color 0.15s ease;
}
.footer-legal a:hover { color: #0e3471; }
.sep { color: #c8d4e0; }

@media (max-width: 600px) {
  .footer-bottom {
    flex-direction: column;
    text-align: center;
  }
}
@media (max-width: 900px) {
  .footer {
    padding: 2.5rem 1.5rem 1.5rem;
  }
  .footer-grid {
    grid-template-columns: 1fr;
    gap: 2rem;
    text-align: center;
  }
  .footer-logo {
    height: 65px;
    margin: 0 auto 1rem;
  }
  .brand-desc { max-width: 100%; }
  .socials { justify-content: center; }
  .accent { margin: 0 auto 0.9rem; }
  .contact-item { justify-content: center; }
  .footer-col ul li { text-align: center; }
}
</style>