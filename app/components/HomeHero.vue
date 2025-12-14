<template>
  <section class="min-h-screen flex items-center justify-center bg-background relative overflow-hidden">
    <img
      src="/images/asset_2.webp"
      alt="Decorazione asset 2"
      class="absolute left-0 bottom-0 w-[320px] max-w-[56vw] md:w-[450px] md:max-w-[68vw] select-none pointer-events-none"
      draggable="false"
      style="z-index: 12;"
    />

    <transition-group
      name="bg-fade"
      tag="div"
      class="absolute inset-0 w-full h-full pointer-events-none"
    >
      <img
        v-for="(img, i) in [currentBg, nextBg].filter(Boolean)"
        :key="imgKey(i)"
        :src="img"
        alt="Sfondo breathing"
        class="home-bg-breathing bg-fade-img absolute inset-0 w-full h-full object-cover z-0 brightness-100"
        :class="['animate-breath']"
        draggable="false"
      />
    </transition-group>

    <div class="relative z-20 flex flex-col items-center gap-7 px-0">
      <h1 class="text-secondary drop-shadow text-center text-3xl md:text-5xl font-extrabold uppercase tracking-wide shadow-primary/40 leading-tight">
        Guidando il futuro del<br />
        <span class="bg-primary/30 text-foreground px-2 py-1 rounded-xl">building italiano</span>
      </h1>
      <p class="text-lg md:text-2xl text-foreground text-center max-w-2xl font-semibold drop-shadow-lg bg-black/20 rounded-xl px-4 py-2">
        Sono leledan06, costruttore Minecraft che trasforma idee in mondi unici. Creo ambientazioni naturali e strutture creative, condividendo il mio lavoro e ispirando altri a scoprire le possibilità di Minecraft.
      </p>
      <NuxtLink to="/portfolio"
        class="inline-flex items-center gap-2 text-lg font-black uppercase bg-primary text-black rounded-xl px-8 py-4 shadow-lg shadow-primary/20 hover:bg-secondary hover:text-black transform hover:scale-105 transition-all duration-300"
      >
        <UIcon name="i-lucide-hammer" class="text-xl" />
        <span>Scopri il mio lavoro</span>
      </NuxtLink>
    </div>
  </section>
</template>

<script lang="ts" setup>
import { ref, onMounted, onBeforeUnmount, computed } from "vue"

const bgImages = [
  "/background/1.webp",
  "/background/2.webp"
]

const currentBgIndex = ref(0)
const nextBgIndex = ref<number|null>(null)
const isCrossfading = ref(false)
let intervalId: number | null = null
let crossfadeTimeout: number | null = null

const currentBg = computed(() => bgImages[currentBgIndex.value])
const nextBg = computed(() => (nextBgIndex.value !== null ? bgImages[nextBgIndex.value] : null))

function imgKey(i: number) {
  if (i === 0) return `bg-${currentBgIndex.value}`
  if (i === 1 && nextBgIndex.value !== null) return `bg-${nextBgIndex.value}`
  return `bg-${i}`
}

function startLoop() {
  intervalId = window.setInterval(() => {
    isCrossfading.value = true
    nextBgIndex.value = (currentBgIndex.value + 1) % bgImages.length

    crossfadeTimeout = window.setTimeout(() => {
      currentBgIndex.value = nextBgIndex.value as number
      nextBgIndex.value = null
      isCrossfading.value = false
    }, 1500)
  }, 4500)
}

onMounted(() => {
  startLoop()
})
onBeforeUnmount(() => {
  if (intervalId) clearInterval(intervalId)
  if (crossfadeTimeout) clearTimeout(crossfadeTimeout)
})
</script>

<style>
.home-bg-breathing {
  position: absolute;
  inset: 0;
  width: 100%;
  height: 100%;
  object-fit: cover;
  pointer-events: none;
  z-index: 0;
}
.bg-fade-img {
  opacity: 1;
  transition: opacity 1.5s cubic-bezier(0.4,0.0,0.2,1);
}
.bg-fade-leave-active {
  transition: opacity 1.5s cubic-bezier(0.4,0.0,0.2,1);
  z-index: 0;
}
.bg-fade-leave-to {
  opacity: 0;
}
.bg-fade-enter-active {
  transition: opacity 1.5s cubic-bezier(0.4,0.0,0.2,1);
  z-index: 0;
}
.bg-fade-enter-from {
  opacity: 0;
}
.bg-fade-enter-to,
.bg-fade-leave-from {
  opacity: 1;
}

@keyframes breath {
  0% { transform: scale(1);}
  50% { transform: scale(1.02);}
  100% { transform: scale(1);}
}
.animate-breath {
  animation: breath 3s ease-in-out infinite;
}
</style>