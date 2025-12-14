<template>
  <div class="min-h-screen bg-background">
    <NavBar class="sticky top-0 z-10 bg-background" />
    <h1 class="text-3xl md:text-5xl font-bold text-primary tracking-wide mb-3 text-center uppercase py-10">Servizi</h1>


    <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-4 pb-10 mx-5">
      <UPricingPlan v-for="plan in plans" :key="plan.title" :title="plan.title" :price="plan.price" :features="plan.features" :badge="plan.badge" variant="soft" :ui="{
        root: 'bg-background-secondary border-2 border-primary shadow-lg shadow-secondary',
        title: 'text-secondary font-bold text-xl uppercase',
        price: 'text-text font-bold text-xl',
        featureTitle: 'text-text',
      }" 
      />
    </div>
  </div>
</template>


<script lang="ts" setup>
const plans = [
    {
      title: "Costruzione",
      price: "€50 - €300+",
      features: [ 
        "Sculture personalizzate",
        "Creature e animali",
        "Figure umane",
        "Consegna in 5-10 giorni"
      ]
    },
    {
      title: "Strutture Avanzate",
      price: "€200 - €500",
      features: [
        "Castelli e fortezze",
        "Città e villaggi",
        "Terraforming incluso",
        "Consegna in 7-14 giorni"
      ]
    },
    {
      title: "Costruzioni Base",
      price: "€50 - €150",
      features: [
        "Case e abitazioni",
        "Piccole strutture",
        "Dettagli personalizzati",
        "Consegna in 3-5 giorni"
      ]
    },
    {
      title: "Terraforming",
      price: "€150 - €400",
      features: [
        "Paesaggi naturali",
        "Montagne e foreste",
        "Flora dettagliata",
        "Consegna in 7-12 giorni"
      ]
    },
    {
      title: "Skin Creation", 
      price: "€20 - €50",
      features: [
        "Skin personalizzate",
        "Alta qualità",
        "Dettagli avanzati",
        "Consegna in 1-3 giorni"
      ]
    },
    {
      title: "Progetti Custom",
      price: "Su Preventivo",
      badge: "Popolare",
      features: [
        "Progetti unici",
        "Server completi",
        "Spawn e lobby",
        "Tempi personalizzati"
      ]
    }
]
</script>

<style>

</style>