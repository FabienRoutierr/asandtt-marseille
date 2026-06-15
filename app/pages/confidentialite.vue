<template>
  <div>
    <section class="section">
      <div class="section-inner">
        <h1>Politique de confidentialité</h1>

        <h2>Responsable du traitement</h2>
        <p>L'association <strong>ASANDTT Marseille</strong>, représentée par Sébastien Malet (Président), est responsable du traitement de vos données personnelles collectées via ce site.</p>

        <h2>Données collectées</h2>
        <p>Lors de l'utilisation du formulaire de contact, les données suivantes sont collectées :</p>
        <ul>
          <li>Prénom et nom</li>
          <li>Adresse email</li>
          <li>Numéro de téléphone</li>
          <li>Contenu du message</li>
        </ul>
        <p>Aucune autre donnée (cookies de tracking, données de navigation, etc.) n'est collectée sur ce site.</p>

        <h2>Finalité du traitement</h2>
        <p>Les données collectées via le formulaire de contact sont utilisées <strong>uniquement</strong> pour répondre à votre demande. Elles sont transmises par email à l'adresse contact.asandtt.marseille@gmail.com et ne sont pas utilisées à des fins commerciales ou publicitaires.</p>

        <h2>Durée de conservation</h2>
        <p>Vos données sont conservées le temps nécessaire au traitement de votre demande, et supprimées au plus tard <strong>12 mois</strong> après votre prise de contact.</p>

        <h2>Destinataires des données</h2>
        <p>Vos données personnelles ne sont transmises à aucun tiers. Elles sont accessibles uniquement par les membres du bureau de l'association dans le cadre du traitement de votre demande.</p>

        <h2>Vos droits</h2>
        <p>Conformément au Règlement Général sur la Protection des Données (RGPD), vous disposez des droits suivants :</p>
        <ul>
          <li><strong>Droit d'accès :</strong> vous pouvez demander à consulter les données vous concernant.</li>
          <li><strong>Droit de rectification :</strong> vous pouvez demander la correction de données inexactes.</li>
          <li><strong>Droit à l'effacement :</strong> vous pouvez demander la suppression de vos données.</li>
          <li><strong>Droit d'opposition :</strong> vous pouvez vous opposer au traitement de vos données.</li>
        </ul>
        <p>Pour exercer ces droits, contactez-nous à l'adresse : <a href="mailto:contact.asandtt.marseille@gmail.com">contact.asandtt.marseille@gmail.com</a></p>

        <h2>Réclamation</h2>
        <p>Si vous estimez que vos droits ne sont pas respectés, vous pouvez adresser une réclamation à la <strong>CNIL</strong> : <a href="https://www.cnil.fr" target="_blank" rel="noopener noreferrer">www.cnil.fr</a></p>

        <h2>Mise à jour</h2>
        <p>Cette politique de confidentialité a été mise à jour le <strong>11 juin 2026</strong>.</p>
      </div>
    </section>
  </div>
</template>

<script setup>
definePageMeta({ layout: 'default' })
useSeoMeta({
  title: 'Politique de confidentialité — ASANDTT Marseille',
  description: 'Politique de confidentialité et protection des données du site ASANDTT Marseille.',
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