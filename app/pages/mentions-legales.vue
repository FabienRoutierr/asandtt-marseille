<template>
  <div>
    <section class="section">
      <div class="section-inner">
        <h1>Mentions légales</h1>

        <h2>Éditeur du site</h2>
        <p>Le présent site est édité par l'association <strong>ASANDTT Marseille</strong>.</p>
        <ul>
          <li><strong>Dénomination :</strong> ASANDTT Marseille</li>
          <li><strong>Adresse :</strong> Gymnase Antonin Artaud, 25 chemin Notre Dame de Consolation, 13013 Marseille</li>
          <li><strong>Téléphone :</strong> 04 91 78 80 00</li>
          <li><strong>Email :</strong> contact.asandtt.marseille@gmail.com</li>
          <li><strong>Responsable de publication :</strong> Sébastien Malet, Président</li>
        </ul>

        <h2>Hébergeur</h2>
        <ul>
          <li><strong>Société :</strong> OVH SAS</li>
          <li><strong>Adresse :</strong> 2 rue Kellermann, 59100 Roubaix, France</li>
          <li><strong>Téléphone :</strong> 1007</li>
          <li><strong>Site web :</strong> <a href="https://www.ovhcloud.com" target="_blank" rel="noopener noreferrer">www.ovhcloud.com</a></li>
        </ul>

        <h2>Propriété intellectuelle</h2>
        <p>L'ensemble du contenu de ce site (textes, images, logos) est la propriété de l'association ASANDTT Marseille ou de ses partenaires. Toute reproduction, même partielle, est interdite sans autorisation préalable.</p>

        <h2>Limitation de responsabilité</h2>
        <p>L'association ASANDTT Marseille s'efforce de maintenir les informations publiées sur ce site à jour et exactes. Elle ne saurait être tenue responsable des erreurs ou omissions, ni des dommages résultant de l'utilisation du site.</p>

        <h2>Droit applicable</h2>
        <p>Le présent site est soumis au droit français. Tout litige relatif à son utilisation relève de la compétence des tribunaux français.</p>
      </div>
    </section>
  </div>
</template>

<script setup>
definePageMeta({ layout: 'default' })
useSeoMeta({
  title: 'Mentions légales — ASANDTT Marseille',
  description: 'Mentions légales du site de l\'association ASANDTT Marseille.',
})
</script>

<style scoped>
.section {
  padding: 5rem 2.5rem;
  background: #fff;
  min-height: 60vh;
}
.section-inner {
  max-width: 800px;
  margin: 0 auto;
}
h1 {
  font-size: 36px;
  font-weight: 700;
  color: #0e3471;
  margin-bottom: 2.5rem;
}
h2 {
  font-size: 18px;
  font-weight: 600;
  color: #0e3471;
  margin-top: 2rem;
  margin-bottom: 0.75rem;
  padding-bottom: 0.5rem;
  border-bottom: 1px solid #e4eaf2;
}
p, li {
  font-size: 15px;
  color: #5a6a7a;
  line-height: 1.75;
}
ul {
  padding-left: 1.25rem;
  margin-bottom: 1rem;
}
li { margin-bottom: 4px; }
a { color: #1455A4; }
a:hover { text-decoration: underline; }

@media (max-width: 900px) {
  .section { padding: 3rem 1.25rem; }
  h1 { font-size: 26px; }
}
</style>