<template>
  <footer class="footer">
    <div class="footer-grid">
      <div class="footer-brand">
        <div class="logo-dot">
          <svg viewBox="0 0 24 24" fill="none" width="20" height="20">
            <circle cx="12" cy="12" r="9" stroke="white" stroke-width="1.8"/>
            <circle cx="12" cy="12" r="3.5" fill="white"/>
          </svg>
        </div>
        <p class="brand-name">ASANDTT Marseille</p>
        <p class="brand-sub">Tennis de table</p>
        <p class="brand-desc">Club affilié à la FFTT, ouvert à tous depuis plus de 40 ans. 20 tables, plusieurs créneaux hebdomadaires, loisir et compétition.</p>
        <div class="socials">
          <a href="#" class="soc" aria-label="Facebook"><svg width="16" height="16" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="1.8"><path d="M18 2h-3a5 5 0 0 0-5 5v3H7v4h3v8h4v-8h3l1-4h-4V7a1 1 0 0 1 1-1h3z"/></svg></a>
          <a href="#" class="soc" aria-label="Instagram"><svg width="16" height="16" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="1.8"><rect x="2" y="2" width="20" height="20" rx="5"/><circle cx="12" cy="12" r="4"/><circle cx="17.5" cy="6.5" r="0.5" fill="currentColor"/></svg></a>
        </div>
      </div>

      <div class="footer-col">
        <div class="accent"></div>
        <h4>Navigation</h4>
        <ul>
          <li><NuxtLink to="/">Accueil</NuxtLink></li>
          <li><NuxtLink to="/club">Le club</NuxtLink></li>
          <li><NuxtLink to="/competitions">Compétitions</NuxtLink></li>
          <li><NuxtLink to="/open-marseille">Open de Marseille</NuxtLink></li>
          <li><NuxtLink to="/inscription">S'inscrire</NuxtLink></li>
        </ul>
      </div>

      <div class="footer-col">
        <div class="accent"></div>
        <h4>Infos pratiques</h4>
        <ul>
          <li><NuxtLink to="/inscription">Tarifs & licences</NuxtLink></li>
          <li><NuxtLink to="/inscription">Horaires</NuxtLink></li>
          <li><NuxtLink to="/contact">Accès</NuxtLink></li>
          <li><NuxtLink to="/partenaires">Partenaires</NuxtLink></li>
          <li><NuxtLink to="/mentions-legales">Mentions légales</NuxtLink></li>
        </ul>
      </div>

      <div class="footer-col">
        <div class="accent"></div>
        <h4>Contact</h4>
        <div class="contact-item">
          <svg width="15" height="15" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="1.8" aria-hidden="true"><path d="M21 10c0 7-9 13-9 13s-9-6-9-13a9 9 0 0 1 18 0z"/><circle cx="12" cy="10" r="3"/></svg>
          <span>Gymnase Artaud<br/>Marseille, France</span>
        </div>
        <div class="contact-item">
          <svg width="15" height="15" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="1.8" aria-hidden="true"><circle cx="12" cy="12" r="10"/><polyline points="12 6 12 12 16 14"/></svg>
          <span>Lun – Ven : 18h – 22h</span>
        </div>
        <div class="contact-item">
          <svg width="15" height="15" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="1.8" aria-hidden="true"><path d="M4 4h16c1.1 0 2 .9 2 2v12c0 1.1-.9 2-2 2H4c-1.1 0-2-.9-2-2V6c0-1.1.9-2 2-2z"/><polyline points="22,6 12,13 2,6"/></svg>
          <span>contact@asandtt-marseille.fr</span>
        </div>
      </div>
    </div>

    <div class="footer-bottom">
      <p>© 2026 ASANDTT Marseille · Tous droits réservés</p>
      <div class="bottom-links">
        <NuxtLink to="/mentions-legales">Mentions légales</NuxtLink>
        <NuxtLink to="/confidentialite">Confidentialité</NuxtLink>
      </div>
    </div>
  </footer>
</template>

<script setup>
</script>

<style scoped>
.footer {
  background: #0d1f3c;
  padding: 3.5rem 2.5rem 1.5rem;
}
.footer-grid {
  display: grid;
  grid-template-columns: 2fr 1fr 1fr 1fr;
  gap: 2rem;
  max-width: 1100px;
  margin: 0 auto 2.5rem;
}
.logo-dot {
  width: 36px; height: 36px;
  background: #1455A4;
  border-radius: 9px;
  display: flex; align-items: center; justify-content: center;
}
.brand-name { font-size: 16px; font-weight: 500; color: #fff; margin-top: 10px; }
.brand-sub { font-size: 11px; color: #5a7a9a; letter-spacing: 1.2px; text-transform: uppercase; }
.brand-desc { font-size: 13px; color: #5a7a9a; line-height: 1.7; margin-top: 0.75rem; max-width: 250px; }
.socials { display: flex; gap: 8px; margin-top: 1.2rem; }
.soc {
  width: 32px; height: 32px;
  border-radius: 7px;
  background: rgba(255,255,255,0.06);
  border: 0.5px solid rgba(255,255,255,0.08);
  display: flex; align-items: center; justify-content: center;
  color: #5a7a9a;
  text-decoration: none;
}
.soc:hover { background: rgba(255,255,255,0.1); color: #fff; }
.footer-col h4 {
  font-size: 11px; color: #fff;
  letter-spacing: 1.5px; text-transform: uppercase;
  margin-bottom: 1rem; font-weight: 500;
}
.footer-col ul { list-style: none; }
.footer-col ul li { margin-bottom: 8px; }
.footer-col ul li a { font-size: 13px; color: #5a7a9a; text-decoration: none; }
.footer-col ul li a:hover { color: #fff; }
.accent { width: 32px; height: 2.5px; background: #1455A4; border-radius: 2px; margin-bottom: 0.9rem; }
.contact-item {
  display: flex; align-items: flex-start; gap: 8px; margin-bottom: 9px;
}
.contact-item svg { color: #1455A4; flex-shrink: 0; margin-top: 2px; }
.contact-item span { font-size: 13px; color: #5a7a9a; line-height: 1.5; }
.footer-bottom {
  border-top: 0.5px solid rgba(255,255,255,0.06);
  padding-top: 1.25rem;
  display: flex; align-items: center; justify-content: space-between;
  max-width: 1100px; margin: 0 auto;
}
.footer-bottom p { font-size: 12px; color: #3a5a7a; }
.bottom-links { display: flex; gap: 16px; }
.bottom-links a { font-size: 12px; color: #3a5a7a; text-decoration: none; }
.bottom-links a:hover { color: #fff; }
</style>