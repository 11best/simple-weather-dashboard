<script setup lang="ts">
defineProps<{
  data: any;
}>();
</script>

<template>
  <div class="bg-white opacity-70 w-full h-full rounded-lg p-2">
    <div class="flex items-center">
      <div class="w-12 h-12 bg-teal-600 rounded-full">{{ data.icon }}</div>
      <p class="font-bold text-sm ml-1">{{ data.title }}</p>
    </div>
    <div class="text-center">
      <span class="font-bold text-3xl">{{ data.value }}</span>
      <span class="ml-1 text-xl">{{ data.unit }}</span>
    </div>
  </div>
</template>
