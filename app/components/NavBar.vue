<template>
  <nav class="flex items-center uppercase py-4 px-4 sm:py-5 sm:px-15 bg-background">
    <!-- Logo -->
    <div>
      <img src="/images/favicon.png" alt="Logo" class="max-h-10 w-auto object-cover drop-shadow" />
    </div>

    <!-- Hamburger button for mobile -->
    <button
      class="ml-auto sm:hidden p-2 rounded focus:outline-none focus:ring-2 focus:ring-primary"
      @click="mobileOpen = !mobileOpen"
      aria-label="Apri il menu di navigazione"
    >
      <UIcon :name="mobileOpen ? 'i-lucide-x' : 'i-lucide-menu'" class="w-8 h-8 text-primary" />
    </button>

    <!-- Desktop menu -->
    <div class="w-full gap-6 flex justify-end sm:flex hidden">
      <div 
        v-for="item in items" 
        :key="item.label" 
        class="flex gap-2 items-center"
      >
        <NuxtLink 
          :to="item.to" 
          class="group relative text-text font-bold hover:text-primary transition-all hover:scale-105 flex items-center gap-2 px-2 py-1 rounded focus:outline-none focus-visible:ring-2 focus-visible:ring-primary"
        >
          <UIcon :name="item.icon" class="text-primary" />
          <span class="hidden md:block relative">
            {{ item.label }}
            <span 
              class="pointer-events-none absolute left-0 -bottom-[0.2em] w-full h-[2px] bg-secondary scale-x-0 group-hover:scale-x-100 origin-left transition-transform duration-300"
            ></span>
          </span>
        </NuxtLink>
      </div>
    </div>

    <!-- Mobile overlay menu -->
    <transition name="fade">
      <div
        v-if="mobileOpen"
        class="fixed inset-0 z-20 bg-black/70 flex flex-col"
        @click.self="mobileOpen = false"
      >
        <nav
          class="bg-background p-6 h-full w-4/5 max-w-xs shadow-xl flex flex-col gap-3"
          role="menu"
          aria-label="Navigazione principale"
        >
          <button
            class="self-end mb-3 p-2 rounded focus:outline-none focus:ring-2 focus:ring-primary"
            @click="mobileOpen = false"
            aria-label="Chiudi il menu"
          >
            <UIcon name="i-lucide-x" class="w-8 h-8 text-primary" />
          </button>
          <div 
            v-for="item in items"
            :key="item.label"
            class="flex items-center gap-2"
            role="menuitem"
          >
            <NuxtLink
              :to="item.to"
              class="flex items-center gap-3 w-full text-lg text-text font-bold py-2 px-2 rounded hover:bg-primary/10 hover:text-primary transition focus:outline-none focus-visible:ring-2 focus-visible:ring-primary"
              @click="mobileOpen = false"
              tabindex="0"
            >
              <UIcon :name="item.icon" class="text-primary" />
              <span>{{ item.label }}</span>
            </NuxtLink>
          </div>
        </nav>
      </div>
    </transition>
  </nav>
</template>



<script lang="ts" setup>
  const mobileOpen = ref(false);
const items = ref([
  {
    label: 'Home',
    to: '/',
    icon: 'i-lucide-home',
  },
  {
    label: 'Chi sono',
    to: '/about',
    icon: 'i-lucide-user',
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