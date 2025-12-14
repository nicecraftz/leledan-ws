<template>
  <nav class="flex items-center uppercase py-5 px-15">
    <div>
      <img src="/images/favicon.png" alt="Logo" class="max-h-10 w-auto object-cover drop-shadow" />
    </div>

    <div class="w-full gap-6 flex justify-end">
      <div 
        v-for="item in items" 
        :key="item.label" 
        class="flex gap-2 items-center"
      >
        <NuxtLink 
          :to="item.to" 
          class="group relative text-text font-bold hover:text-primary transition-all hover:scale-105 flex items-center gap-2"
        >
          <!-- Icona rimossa dalla linea sottolineata -->
          <UIcon :name="item.icon" class="text-primary" />
          <span class="hidden md:block relative">
            {{ item.label }}
            <!-- Animated underline on hover SOLO sotto il testo -->
            <span 
              class="pointer-events-none absolute left-0 -bottom-[0.2em] w-full h-[2px] bg-secondary scale-x-0 group-hover:scale-x-100 origin-left transition-transform duration-300"
            ></span>
          </span>
        </NuxtLink>
      </div>
    </div>
  </nav>
</template>



<script lang="ts" setup>
const items = ref([
  {
    label: 'Home',
    to: '/',
    icon: 'i-lucide-home',
  },
  {
    label: 'Servizi',
    to: '/services',
    icon: 'i-lucide-hammer',
  },
  {
    label: 'Portfolio',
    to: '/portfolio',
    icon: 'i-lucide-image',
  },
  {
    label: 'Recensioni',
    to: '/reviews',
    icon: 'i-lucide-star',
  },
  {
    label: 'TOS',
    to: '/tos',
    icon: 'i-lucide-file-text',
  }
]);

</script>

<style>

</style>