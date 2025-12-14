<template>
  <div class="bg-background p-4">
    <h1 class="text-2xl font-bold text-primary tracking-wide mb-5 text-center">Competenze Tecniche</h1>
    <div class="flex flex-wrap gap-10 justify-center iems-center">
      <SkillIcon v-for="skill in skills" :key="skill.title" :icon="skill.icon" :title="skill.title" :description="skill.description" />
    </div>
  </div>
</template>

<script lang="ts" setup>
  const skills = [
    {
      icon: "i-lucide-trees",
      title: "Organiche",
      description: "Sculture, Animali, Umani realizzati nel dettaglio"
    },
    {
      icon: "i-lucide-compass",
      title: "Botanica",
      description: "Virtuale Flora realistica e atmosfera spettacolare"
    },
    {
      icon: "i-lucide-mountain",
      title: "Scultura Terreni",
      description: "Terraforming Dettagliato e professionale"
    },
    {
      icon: "i-lucide-house",
      title: "Architettura",
      description: "Stili architettonici di qualsiasi tipo"
    },
    {
      icon: "i-lucide-lightbulb",
      title: "Illuminazione",
      description: "Esperto in light making nelle build"
    },
    {
      icon: "i-lucide-clapperboard",
      title: "Video Editing",
      description: "Montaggio e produzione YouTube per condividere il mio lavoro"
    },
    {
      icon: "i-lucide-user-round",
      title: "Skin Making",
      description: "Skin create nel dettaglio"
    }
  ]
</script>

<style>

</style>