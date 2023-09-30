<script setup lang="ts">
defineProps<{
  title: string;
}>();
</script>

<template>
  <div
    class="bg-white opacity-80 w-full rounded-full text-center font-bold text-2xl py-1"
  >
    {{ title }}
  </div>
</template>
