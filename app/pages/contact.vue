<script setup>
definePageMeta({ layout: 'default' })

useSeoMeta({
  title: 'Nous contacter — ASANDTT Marseille',
  description: 'Contactez le club ASANDTT Marseille, gymnase Antonin Artaud, 13013 Marseille.',
})

const form = ref({
  prenom: '',
  nom: '',
  email: '',
  telephone: '',
  message: ''
})

const submitted = ref(false)

function handleSubmit() {
  submitted.value = true
}
</script>

<template>
  <div>

    <!-- CONTENU -->
    <section class="section section-white">
      <div class="section-inner content-grid">

        <!-- COLONNE GAUCHE : infos + tarifs + map -->
        <div class="left-col">

          <!-- INFOS PRATIQUES -->
          <div class="info-card">
            <h3>Contact</h3>
            <div class="info-item">
              <svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="1.5"><path d="M22 16.92v3a2 2 0 0 1-2.18 2 19.79 19.79 0 0 1-8.63-3.07A19.5 19.5 0 0 1 4.69 12a19.79 19.79 0 0 1-3.07-8.67A2 2 0 0 1 3.6 1.27h3a2 2 0 0 1 2 1.72c.127.96.361 1.903.7 2.81a2 2 0 0 1-.45 2.11L7.91 8.91a16 16 0 0 0 6 6l.95-.95a2 2 0 0 1 2.11-.45c.907.339 1.85.573 2.81.7A2 2 0 0 1 22 16.92z"/></svg>
              <div>
                <strong>Téléphone</strong>
                <span>04 91 78 80 00</span>
              </div>
            </div>
            <div class="info-item">
              <svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="1.5"><path d="M21 10c0 7-9 13-9 13s-9-6-9-13a9 9 0 0 1 18 0z"/><circle cx="12" cy="10" r="3"/></svg>
              <div>
                <strong>Adresse</strong>
                <span>Gymnase Antonin Artaud<br/>25 chemin Notre Dame de Consolation<br/>13013 Marseille</span>
              </div>
            </div>
            <div class="info-item">
              <svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="1.5"><circle cx="12" cy="12" r="10"/><polyline points="12 6 12 12 16 14"/></svg>
              <div>
                <strong>Horaires</strong>
                <span>Lun – Ven : 17h30 – 21h<br/>Mercredi après-midi et vendredi soir pour les enfants<br/>Samedi : compétitions</span>
              </div>
            </div>
          </div>

          <!-- TARIFS -->
          <div class="tarifs-card">
            <h3>Tarifs</h3>
            <div class="tarif-item">
              <div class="tarif-label">
                <span class="tarif-dot competition"></span>
                <span>Compétiteur</span>
              </div>
              <span class="tarif-price">À définir</span>
            </div>
            <div class="tarif-item">
              <div class="tarif-label">
                <span class="tarif-dot jeune"></span>
                <span>Jeune</span>
              </div>
              <span class="tarif-price">À définir</span>
            </div>
            <div class="tarif-item">
              <div class="tarif-label">
                <span class="tarif-dot loisir"></span>
                <span>Loisir</span>
              </div>
              <span class="tarif-price">À définir</span>
            </div>
            <p class="tarif-note">Les inscriptions sont possibles toute l'année.</p>
          </div>

          <!-- MAP -->
          <div class="map-card">
            <h3>Accès au gymnase</h3>
            <div class="map-wrap">
              <iframe
                src="https://www.google.com/maps/embed?pb=!1m18!1m12!1m3!1d2904.123456789!2d5.4197!3d43.3209!2m3!1f0!2f0!3f0!3m2!1i1024!2i768!4f13.1!3m3!1m2!1s0x0%3A0x0!2zNDPCsDE5JzE1LjIiTiA1wrAyNScxMC45IkU!5e0!3m2!1sfr!2sfr!4v1234567890"
                width="100%"
                height="220"
                style="border:0; border-radius: 12px;"
                allowfullscreen=""
                loading="lazy"
                referrerpolicy="no-referrer-when-downgrade"
                title="Gymnase Antonin Artaud Marseille"
              ></iframe>
            </div>
            
              <a href="https://maps.google.com/?q=Gymnase+Antonin+Artaud+25+chemin+Notre+Dame+de+Consolation+13013+Marseille"
              target="_blank"
              class="map-link"
            >
              <svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="1.5"><path d="M21 10c0 7-9 13-9 13s-9-6-9-13a9 9 0 0 1 18 0z"/><circle cx="12" cy="10" r="3"/></svg>
              Ouvrir dans Google Maps
            </a>
          </div>

        </div>

        <!-- COLONNE DROITE : formulaire -->
        <div class="right-col">
          <div class="form-card">
            <h3>Nous contacter</h3>

            <div v-if="submitted" class="success-msg">
              <svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="1.5"><path d="M22 11.08V12a10 10 0 1 1-5.93-9.14"/><polyline points="22 4 12 14.01 9 11.01"/></svg>
              <div>
                <strong>Message envoyé !</strong>
                <span>Nous vous répondrons très bientôt.</span>
              </div>
            </div>

            <form v-else @submit.prevent="handleSubmit" class="contact-form">
              <div class="form-row">
                <div class="form-group">
                  <label>Prénom <span class="required">*</span></label>
                  <input v-model="form.prenom" type="text" placeholder="Votre prénom" required />
                </div>
                <div class="form-group">
                  <label>Nom <span class="required">*</span></label>
                  <input v-model="form.nom" type="text" placeholder="Votre nom" required />
                </div>
              </div>
              <div class="form-group">
                <label>Adresse email <span class="required">*</span></label>
                <input v-model="form.email" type="email" placeholder="votre@email.com" required />
              </div>
              <div class="form-group">
                <label>Numéro de téléphone <span class="required">*</span></label>
                <input v-model="form.telephone" type="tel" placeholder="06 XX XX XX XX" required />
              </div>
              <div class="form-group">
                <label>Message <span class="required">*</span></label>
                <textarea v-model="form.message" rows="6" placeholder="Votre message..." required></textarea>
              </div>
              <button type="submit" class="btn-submit">
                <svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="1.5"><line x1="22" y1="2" x2="11" y2="13"/><polygon points="22 2 15 22 11 13 2 9 22 2"/></svg>
                Envoyer le message
              </button>
            </form>
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

/* LAYOUT */
.section { padding: 5rem 2.5rem; }
.section-white { background: #f7f9fc; }
.section-inner { max-width: 1200px; margin: 0 auto; }

.content-grid {
  display: grid;
  grid-template-columns: 1fr 1fr;
  gap: 2rem;
  align-items: start;
}

/* CARDS COMMUNES */
.info-card, .tarifs-card, .map-card, .form-card {
  background: #fff;
  border: 0.5px solid #e4eaf2;
  border-radius: 16px;
  padding: 1.75rem;
  box-shadow: 0 4px 16px rgba(10,30,70,0.06);
}
.left-col {
  display: flex;
  flex-direction: column;
  gap: 1.5rem;
}
.info-card h3, .tarifs-card h3, .map-card h3, .form-card h3 {
  font-size: 18px;
  font-weight: 600;
  color: #0d1f3c;
  margin-bottom: 1.25rem;
}

/* INFO ITEMS */
.info-item {
  display: flex;
  align-items: flex-start;
  gap: 12px;
  margin-bottom: 1rem;
}
.info-item:last-child { margin-bottom: 0; }
.info-item svg {
  width: 18px;
  height: 18px;
  color: #1455A4;
  flex-shrink: 0;
  margin-top: 2px;
}
.info-item div {
  display: flex;
  flex-direction: column;
  gap: 3px;
}
.info-item strong {
  font-size: 13px;
  font-weight: 600;
  color: #0d1f3c;
}
.info-item span {
  font-size: 13px;
  color: #5a6a7a;
  line-height: 1.5;
}

/* TARIFS */
.tarif-item {
  display: flex;
  align-items: center;
  justify-content: space-between;
  padding: 0.75rem 0;
  border-bottom: 0.5px solid #f0f4f8;
}
.tarif-item:last-of-type { border-bottom: none; }
.tarif-label {
  display: flex;
  align-items: center;
  gap: 10px;
  font-size: 14px;
  color: #3d4f63;
  font-weight: 500;
}
.tarif-dot {
  width: 10px;
  height: 10px;
  border-radius: 50%;
  flex-shrink: 0;
}
.tarif-dot.competition { background: #1455A4; }
.tarif-dot.jeune { background: #22c55e; }
.tarif-dot.loisir { background: #f59e0b; }
.tarif-price {
  font-size: 14px;
  font-weight: 600;
  color: #0d1f3c;
}
.tarif-note {
  font-size: 12px;
  color: #8899aa;
  margin-top: 1rem;
  line-height: 1.5;
  font-style: italic;
}

/* MAP */
.map-wrap { margin-bottom: 0.75rem; }
.map-link {
  display: inline-flex;
  align-items: center;
  gap: 6px;
  font-size: 13px;
  color: #1455A4;
  text-decoration: none;
  font-weight: 500;
}
.map-link svg { width: 15px; height: 15px; }
.map-link:hover { text-decoration: underline; }

/* FORM */
.form-subtitle {
  font-size: 14px;
  color: #5a6a7a;
  margin-bottom: 1.75rem;
}
.contact-form {
  display: flex;
  flex-direction: column;
  gap: 1.1rem;
}
.form-row {
  display: grid;
  grid-template-columns: 1fr 1fr;
  gap: 1rem;
}
.form-group {
  display: flex;
  flex-direction: column;
  gap: 6px;
}
.form-group label {
  font-size: 13px;
  font-weight: 600;
  color: #0d1f3c;
}
.required { color: #1455A4; }
.form-group input,
.form-group textarea {
  border: 1px solid #e4eaf2;
  border-radius: 8px;
  padding: 10px 14px;
  font-size: 14px;
  color: #0d1f3c;
  background: #fff;
  outline: none;
  transition: border-color 0.15s ease;
  font-family: inherit;
  resize: none;
}
.form-group input:focus,
.form-group textarea:focus {
  border-color: #1455A4;
  box-shadow: 0 0 0 3px rgba(20,85,164,0.08);
}
.btn-submit {
  display: flex;
  align-items: center;
  justify-content: center;
  gap: 8px;
  background: #3293d4;
  color: #fff;
  border: none;
  padding: 13px 28px;
  border-radius: 8px;
  font-size: 15px;
  font-weight: 600;
  cursor: pointer;
  transition: background 0.15s ease, box-shadow 0.15s ease;
  box-shadow: 0 4px 12px rgba(20,85,164,0.3);
  font-family: inherit;
}
.btn-submit svg { width: 16px; height: 16px; }
.btn-submit:hover {
  background: #0f3f85;
  box-shadow: 0 6px 18px rgba(20,85,164,0.4);
}

/* SUCCESS */
.success-msg {
  display: flex;
  align-items: center;
  gap: 14px;
  background: #e8f5e9;
  border: 0.5px solid #a5d6a7;
  border-radius: 10px;
  padding: 1.25rem;
}
.success-msg svg {
  width: 28px;
  height: 28px;
  color: #2e7d32;
  flex-shrink: 0;
}
.success-msg div {
  display: flex;
  flex-direction: column;
  gap: 3px;
}
.success-msg strong {
  font-size: 15px;
  font-weight: 600;
  color: #1b5e20;
}
.success-msg span {
  font-size: 13px;
  color: #388e3c;
}
</style>