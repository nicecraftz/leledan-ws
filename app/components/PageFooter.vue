<template>
  <footer class="py-3 border-t-5 border-primary bg-background">
    <div class="flex justify-center items-center gap-4 flex-col">
      <div class="flex flex-col items-center">
        <p class="text-text">Copyright © {{new Date().getFullYear()}} leledan06 - Tutti i diritti riservati.</p>
        <p class="text-text italic">Creando nuove realtà, un blocco alla volta.</p>
      </div>

      <div class="flex justify-center items-center gap-3 text-primary py-2">
        <a
          v-for="link in links"
          :key="link.url"
          :href="link.url"
          target="_blank"
          class="flex items-center justify-center duration-300 group hover:scale-105 transition-all"
        >
          <span class="relative flex items-center justify-center">
            <svg
              class="absolute inset-0 w-10 h-10 pointer-events-none blur-xl z-0 color-secondary"
            >
              <use href="/resources/glow_shape.svg" />
            </svg>
            <UIcon
              :name="link.icon"
              size="24"
              class="relative z-10 group-hover:text-secondary transition-colors duration-300"
            />
          </span>
        </a>
      </div>

    </div>
  </footer>
</template>

<script lang="ts" setup>
  const links = [
    {
      icon: "i-simple-icons-discord",
      url: "https://discord.gg/u9FyUqa6uz",
    },
    {
      icon: "i-simple-icons-twitter",
      url: "https://twitter.com/leledan06",
    },
    {
      icon: "i-simple-icons-instagram",
      url: "https://www.instagram.com/leledan.builds/",
    },
    {
      icon: "i-simple-icons-youtube",
      url: "https://www.youtube.com/@leledan06",
    },
    {
      icon: "i-simple-icons-gmail",
      url: "mailto:leledanbusiness@gmail.com",
    },
    {
      icon: "i-simple-icons-telegram",
      url: "https://t.me/leledan06",
    },
    {
      icon: "i-simple-icons-tiktok",
      url: "https://www.tiktok.com/@leledan06",
    }
  ]

</script>