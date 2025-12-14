<template>
  <div class="flex items-center gap-6 p-5 rounded-3xl shadow-lg min-w-64">
    <img 
      :src="image" 
      :alt="name" 
      class="w-20 h-20 rounded-full object-cover border-2 border-primary shadow-md glow-border"
    />
    <!-- Details -->
    <div class="flex flex-col justify-center min-w-0">
      <span class="text-secondary font-semibold text-2xl truncate">{{ name }}</span>
      <span class="text-white font-bold text-base truncate">{{ detail }}</span>
      <span class="text-gray-400 text-sm font-medium mt-2 truncate">{{ counter }}</span>
    </div>
  </div>
</template>

<script lang="ts" setup>
  const props = defineProps<{
    image: string;
    name: string;
    detail: string;
    counter: string;
  }>();
</script>

<style>
.glow-border {
  box-shadow:
    0 0 0 4px var(--color-primary), /* fallback if --color-primary not set */
    0 0 16px 4px var(--color-primary),
    0 0 32px 8px rgba(192,132,252,0.25); /* Soft outer glow */
}
</style>