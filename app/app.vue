<script setup>
useSeoMeta({
  title: 'ASANDTT Marseille — Tennis de table',
  description: 'Club de tennis de table à Marseille. Tous niveaux, tous âges. Loisir et compétition.',
  ogTitle: 'ASANDTT Marseille — Tennis de table',
  ogDescription: 'Club de tennis de table à Marseille. Tous niveaux, tous âges. Loisir et compétition.',
})
useHead({
    meta: [
    { name: 'color-scheme', content: 'light' }
  ],
  link: [
    { rel: 'preconnect', href: 'https://fonts.googleapis.com' },
    { rel: 'preconnect', href: 'https://fonts.gstatic.com', crossorigin: '' },
    { rel: 'stylesheet', href: 'https://fonts.googleapis.com/css2?family=Barlow+Condensed:wght@600;700&family=Montserrat:wght@400;500;600&display=swap' }
  ]
})
</script>

<template>
  <UApp>
    <NuxtLayout>
      <NuxtPage />
    </NuxtLayout>
  </UApp>
</template>