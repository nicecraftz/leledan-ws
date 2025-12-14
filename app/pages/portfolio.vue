<template>
  <div class="bg-background min-h-screen">
    <NavBar class="sticky top-0 z-10 bg-background"/>

    <h1 class="text-3xl md:text-5xl font-bold text-primary tracking-wide mb-3 text-center uppercase my-10">Portfolio</h1>
    <div class="grid grid-cols-1 sm:grid-cols-2 md:grid-cols-3 gap-0 w-full max-w-5xl mx-auto py-14 px-2 min-h-75">
      <div
        v-for="index in portfolioCount"
        :key="index"
        class="group relative"
      >
        <img
          :src="`/portfolio/${(portfolioCount + 1) - index}.webp`"
          alt="Minecraft build example"
          class="aspect-square w-full h-auto object-cover border-2 border-primary group-hover:border-secondary cursor-pointer pointer-events-auto transition-all duration-300"
          draggable="false"
          @click="openPopup((portfolioCount + 1) - index)"
        />
        <div
          class="absolute inset-0 flex items-center justify-center bg-gray-800/45 opacity-0 group-hover:opacity-100 transition-opacity duration-300 pointer-events-none"
        >
          <UIcon name="i-lucide-eye" class="text-4xl text-white drop-shadow" />
        </div>
      </div>
    </div>
    
    <div
      v-if="popupImg !== null"
      class="fixed inset-0 bg-black/80 flex items-center justify-center z-50 transition-all"
      @click.self="closePopup"
    >
      <img
        :src="`/portfolio/${popupImg}.webp`"
        alt="Minecraft build full-size"
        class="max-w-full max-h-[90vh] rounded-2xl shadow-2xl border-4 border-primary bg-background animate-fade-in"
        @click.stop
      />
      <button
        class="absolute top-5 right-8 text-white text-3xl font-extrabold bg-black bg-opacity-40 hover:bg-opacity-70 rounded-full px-3 py-0 transition"
        @click="closePopup"
        aria-label="Chiudi"
      >
        &times;
      </button>
    </div>
  </div>
</template>

<script lang="ts" setup>
  import { ref } from 'vue'

  const portfolioCount = ref(45)
  const popupImg = ref<number|null>(null)

  const openPopup = (imgNum: number) => {
    popupImg.value = imgNum
  }
  const closePopup = () => {
    popupImg.value = null
  }
</script>