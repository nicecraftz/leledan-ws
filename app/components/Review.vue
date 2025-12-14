<template>
  <div class="w-full flex justify-center">
    <div
      id="customer"
      class="flex flex-col md:flex-row items-center justify-center gap-8 w-full max-w-3xl"
      :class="reversed ? 'md:flex-row-reverse' : ''"
    >
      <!-- Immagine e dettagli del cliente -->
      <div id="customer_details" class="flex flex-col items-center gap-2 pt-3 min-w-[176px]">
        <div class="w-40 h-40 rounded-full overflow-hidden flex items-center justify-center border-4 border-secondary hover:-rotate-10 transition-all duration-300 hover:shadow-[0_0_24px_8px_theme('colors.secondary')]">
          <img
            :src="image"
            :alt="name"
            class="w-full h-full object-cover"
          />
        </div>
        <h2 class="text-2xl font-bold text-secondary hover:scale-120 transition-all duration-300 text-center">{{ name }}</h2>
        <p class="text-sm text-white text-center">{{ detail }}</p>
        <p class="text-xs text-white/80 text-center">{{ counter }}</p>
      </div>
      <!-- Box review centrato -->
      <div
        id="review"
        class="flex flex-col items-center justify-center gap-4 bg-background-secondary rounded-lg p-5 border-2 border-primary flex-1"
      >
        <p class="text-text text-center italic text-xl">"{{ review }}"</p>
        <div class="flex gap-2">
          <UIcon name="i-heroicons-star-solid" class="w-6 h-6 text-secondary hover:scale-120 transition-all duration-300" v-for="n in 5" :key="n" />
        </div>
      </div>
    </div>
  </div>
</template>

<script lang="ts" setup>
defineProps<{
  image: string
  name: string
  detail: string
  counter: string
  review: string
  reversed: boolean
}>()
</script>