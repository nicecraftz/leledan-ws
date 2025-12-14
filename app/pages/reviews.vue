<template>
  <div class="min-h-screen bg-background">
    <NavBar class="sticky top-0 z-10 bg-background" />
    <h1 class="text-3xl md:text-5xl font-bold text-primary tracking-wide mb-3 text-center uppercase my-10">Recensioni</h1>
    <div class="flex flex-col items-center w-full py-10">
      <div class="w-full max-w-3xl flex flex-col items-center gap-8">
        <Review 
          v-for="(review,index) in reviews"
          :key="review.name"
          :image="review.image"
          :name="review.name"
          :detail="review.detail"
          :counter="review.counter"
          :review="review.review"
          :reversed="index % 2 === 1"
        />
      </div>
    </div>
  </div>
</template>

<script setup lang="ts">
const reviews = [
    {
      image: "/customers/customer_8.webp",
      name: "Zenith",
      detail: "Youtuber",
      counter: "300k Iscritti",
      review: "Questa costruzione di Minecraft è uno straordinario esempio di creatività e maestria, che mostra una notevole attenzione ai dettagli e al design. La perfetta integrazione tra struttura e ambiente crea un'esperienza coinvolgente che mette in evidenza l'abilità del costruttore."

    },
    {
      image: "/customers/customer_4.webp",
      name: "Divvy",
      detail: "Youtuber",
      counter: "202k Iscritti",
      review: "Ottimo builder, ha realizzato esattamente quello che volevo in tempi rapidi."
    },
    {
      image: "/customers/customer_2.webp",
      name: "Cypro",
      detail: "Youtuber",
      counter: "41,3k Iscritti",
      review: "Ha realizzato per me un piccolo dungeon e ha completamente rinnovato una mia vecchia struttura. Molto veloce e con aggiornamenti costanti, è stato esattamente tutto ciò che avevo chiesto!"
    },
    {
      image: "/customers/customer_1.webp",
      name: "CoralMC",
      detail: "Server",
      counter: "1000 utenti/giorno",
      review: "Ha rispettato completamente i nostri requisiti, è stato disponibile, professionale e puntuale. È anche davvero bravo nella costruzione. Lo consiglio a tutti."
    },
    {
      image: "/customers/customer_3.webp",
      name: "Gabby16bit",
      detail: "Youtuber",
      counter: "3,5M Iscritti",
      review: "Ottimo builder, mi ha realizzato alcune costruzioni per il mio canale YouTube. Professionale, veloce e talentuoso."
    },
  ]
</script>