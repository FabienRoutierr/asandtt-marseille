<template>
  <footer class="footer">
    <div class="footer-grid">
      <div class="footer-brand">
        <p class="brand-name">ASANDTT Marseille</p>
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

      <div class="footer-col">
        <div class="accent"></div>
        <h4>Contact</h4>
        <div class="contact-item">
          <svg width="15" height="15" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="1.8" aria-hidden="true"><path d="M21 10c0 7-9 13-9 13s-9-6-9-13a9 9 0 0 1 18 0z"/><circle cx="12" cy="10" r="3"/></svg>
          <span>Gymnase Antonin Artaud<br/>25 chemin Notre Dame de Consolation<br/>13013 Marseille</span>
        </div>
        <div class="contact-item">
          <svg width="15" height="15" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="1.8" aria-hidden="true"><circle cx="12" cy="12" r="10"/><polyline points="12 6 12 12 16 14"/></svg>
          <span>Lun – Ven : 17h30 – 21h</span>
        </div>
        <div class="contact-item">
          <svg width="15" height="15" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="1.8" aria-hidden="true"><path d="M22 16.92v3a2 2 0 0 1-2.18 2 19.79 19.79 0 0 1-8.63-3.07A19.5 19.5 0 0 1 4.69 12a19.79 19.79 0 0 1-3.07-8.67A2 2 0 0 1 3.6 1.27h3a2 2 0 0 1 2 1.72c.127.96.361 1.903.7 2.81a2 2 0 0 1-.45 2.11L7.91 8.91a16 16 0 0 0 6 6l.95-.95a2 2 0 0 1 2.11-.45c.907.339 1.85.573 2.81.7A2 2 0 0 1 22 16.92z"/></svg>
          <span>04 91 78 80 00</span>
        </div>
        <div class="contact-item">
          <svg width="15" height="15" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="1.8" aria-hidden="true"><path d="M4 4h16c1.1 0 2 .9 2 2v12c0 1.1-.9 2-2 2H4c-1.1 0-2-.9-2-2V6c0-1.1.9-2 2-2z"/><polyline points="22,6 12,13 2,6"/></svg>
          <span>contact@asandtt-marseille.fr</span>
        </div>
      </div>
    </div>
  </footer>
</template>

<script setup>
</script>

<style scoped>
.footer {
  background: #1455A4;
  padding: 3.5rem 2.5rem 2rem;
}
.footer-grid {
  display: grid;
  grid-template-columns: 2fr 1fr 1fr;
  gap: 3rem;
  max-width: 1100px;
  margin: 0 auto;
}
.logo-dot {
  width: 36px; height: 36px;
  background: rgba(255,255,255,0.2);
  border-radius: 9px;
  display: flex; align-items: center; justify-content: center;
}
.brand-name { font-size: 16px; font-weight: 500; color: #fff; margin-top: 10px; }
.brand-sub { font-size: 11px; color: rgba(255,255,255,0.6); letter-spacing: 1.2px; text-transform: uppercase; }
.brand-desc { font-size: 13px; color: rgba(255,255,255,0.7); line-height: 1.7; margin-top: 0.75rem; max-width: 280px; }
.socials { display: flex; gap: 8px; margin-top: 1.2rem; }
.soc {
  width: 34px; height: 34px;
  border-radius: 8px;
  background: rgba(255,255,255,0.12);
  border: 0.5px solid rgba(255,255,255,0.2);
  display: flex; align-items: center; justify-content: center;
  color: rgba(255,255,255,0.8);
  text-decoration: none;
  transition: background 0.15s ease;
}
.soc:hover { background: rgba(255,255,255,0.25); color: #fff; }
.footer-col h4 {
  font-size: 11px; color: #fff;
  letter-spacing: 1.5px; text-transform: uppercase;
  margin-bottom: 1rem; font-weight: 600;
}
.footer-col ul { list-style: none; }
.footer-col ul li { margin-bottom: 8px; }
.footer-col ul li a { font-size: 13px; color: rgba(255,255,255,0.7); text-decoration: none; transition: color 0.15s ease; }
.footer-col ul li a:hover { color: #fff; }
.accent { width: 32px; height: 2.5px; background: rgba(255,255,255,0.4); border-radius: 2px; margin-bottom: 0.9rem; }
.contact-item {
  display: flex; align-items: flex-start; gap: 8px; margin-bottom: 10px;
}
.contact-item svg { color: rgba(255,255,255,0.6); flex-shrink: 0; margin-top: 2px; }
.contact-item span { font-size: 13px; color: rgba(255,255,255,0.7); line-height: 1.5; }
</style>