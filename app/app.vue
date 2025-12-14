<template>
  <div>
    <UApp>
      <NuxtLayout>
        <NuxtPage />
      </NuxtLayout>
    </UApp>
  </div>
</template>

<script setup lang="ts">
useSeoMeta({
  title: 'leledan06 | Minecraft Builder Portfolio',
  description: 'Portfolio professionale di leledan06, costruttore Minecraft specializzato in sculture organiche, terraforming e strutture epiche. Scopri servizi, recensioni, galleria lavori e informazioni su come commissionare un progetto.',
  ogTitle: 'leledan06 | Minecraft Builder Portfolio',
  ogDescription: 'Scopri il talento di leledan06: portfolio di progetti Minecraft, servizi personalizzati, galleria immagini, prezzi trasparenti e testimonianze clienti.',
  ogType: 'website',
  twitterCard: 'summary_large_image',
  twitterTitle: 'leledan06 | Minecraft Builder',
  twitterDescription: 'Costruttore Minecraft professionista, esperto in organico, terraforming e architettura. Guarda il portfolio e scopri i miei servizi in Minecraft.',
})

useHead({
  link: [
    { rel: 'icon', type: 'image/svg+xml', href: '/favicon.svg' },
    { rel: 'alternate icon', type: 'image/png', href: '/favicon.png' }
  ],
  meta: [
    { name: 'author', content: 'Alessandro Maria Calista' },
    { name: 'robots', content: 'index, follow' },
    { name: 'keywords', content: 'Minecraft, builder, portfolio, servizi, costruttore, organico, terraforming, architettura, sculture, skin, progetti Minecraft' },
    { property: 'og:url', content: 'https://leledan06.it' }
  ],
  title: 'leledan06 | Minecraft Builder Portfolio'
})
</script>
