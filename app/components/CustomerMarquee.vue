<template>
  <div class="bg-background p-4">
    <h1 class="text-2xl font-bold text-primary tracking-wide mb-5 text-center">
      Clienti e Collaboratori
    </h1>
    <UMarquee :overlay="false" class="p-4" :pauseOnHover="true">
      <CustomerCard
        v-for="customer in customers"
        :key="customer.name"
        :image="customer.image"
        :name="customer.name"
        :detail="customer.detail"
        :counter="customer.counter"
        :link="customer.link"
      />
    </UMarquee>
  </div>
</template>

<script lang="ts" setup>
const customers = [
  {
    image: "/customers/customer_8.webp",
    name: "Zenith",
    detail: "Youtuber",
    counter: "300k Iscritti",
    link: "https://www.youtube.com/@zenithminecraft",
  },
  {
    image: "/customers/customer_4.webp",
    name: "Divvy",
    detail: "Youtuber",
    counter: "202k Iscritti",
    link: "https://www.youtube.com/@divvyminecraft",
  },
  {
    image: "/customers/customer_2.webp",
    name: "Cypro",
    detail: "Youtuber",
    counter: "41,3k Iscritti",
    link: "https://www.youtube.com/@cyproh",
  },
  {
    image: "/customers/customer_1.webp",
    name: "CoralMC",
    detail: "Server",
    counter: "1000 utenti/giorno",
    link: "https://coralmc.it",
  },
  {
    image: "/customers/customer_10.webp",
    name: "Tigr8",
    detail: "Youtuber",
    counter: "148k Iscritti",
    link: "https://www.youtube.com/@Tigr8",
  },
  {
    image: "/customers/customer_6.webp",
    name: "LilyGumdrop",
    detail: "Youtuber",
    counter: "1,64M Iscritti",
    link: "https://www.youtube.com/@Lilygumdrop-rb",
  },
  {
    image: "/customers/customer_5.webp",
    name: "Dungeon Dodge",
    detail: "Server",
    counter: "100 utenti/giorno",
    link: "https://dungeondodge.tebex.io",
  },
  {
    image: "/customers/customer_7.webp",
    name: "yeslucid",
    detail: "Youtuber",
    counter: "198k Iscritti",
    link: "https://www.youtube.com/@yeslucid",
  },
  {
    image: "/customers/customer_9.webp",
    name: "OnMod",
    detail: "Youtuber",
    counter: "18,2k Iscritti",
    link: "https://www.youtube.com/@OnMod",
  },
  {
    image: "/customers/customer_3.webp",
    name: "Gabby16bit",
    detail: "Youtuber",
    counter: "3,5M Iscritti",
    link: "https://www.youtube.com/@Gabby16bit",
  },
];
</script>
