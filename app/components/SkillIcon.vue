<template>
  <div>
    <UPopover mode="hover" :ui="{
      content: 'ring-0 bg-background border-2 border-primary rounded-xl'
    }">
      <div class="w-10 h-10 cursor-pointer group transition-all duration-300 hover:scale-105">
        <UIcon :name="icon" class="text-primary h-full w-full group-hover:text-secondary transition-all duration-300" />
      </div>
      <template #content>
        <div class="h-full w-full rounded-xl p-3">
          <h3 class="text-primary font-bold text-lg text-center">{{ title }}</h3>
          <p class="text-text">{{ description }}</p>
        </div>
      </template>
    </UPopover>
  </div>
</template>

<script lang="ts" setup>
  const props = defineProps<{
    icon: string;
    title: string;
    description: string;
  }>();
</script>

<style>

</style>