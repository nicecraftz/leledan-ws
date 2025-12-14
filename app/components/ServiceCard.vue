<template>
  <div class="border-2 border-secondary rounded-lg p-4 bg-background-secondary shadow-lg shadow-primary hover:-translate-y-1 transition-all duration-300">
    <h2 class="text-xl font-bold text-secondary text-center uppercase">{{ title }}</h2>
    <div class="w-full text-center text-text font-bold text-xl">
      {{ priceRange }}
    </div>
    <ul>
      <li v-for="detail in details" :key="detail" class="flex items-center gap-2 mb-2">
        <UIcon name="i-lucide-check-circle" class="text-secondary" dynamic />
        <span class="text-text">{{ detail }}</span>
      </li>
    </ul>
  </div>
</template>

<script lang="ts" setup>
const props = defineProps<{
  title: string,
  priceRange: string,
  details: string[]
}>();
const { title, priceRange, details } = props
</script>