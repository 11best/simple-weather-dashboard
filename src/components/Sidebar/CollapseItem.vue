<script setup lang="ts">
defineProps<{
  menuItem: { title: string };
}>();
</script>

<template>
  <li
    class="cursor-pointer hover:bg-slate-300 px-4 py-2 flex items-center border-b border-slate-200"
  >
    <div class="bg-green-300 w-6 h-6 rounded-full"></div>
    <p class="ml-2">{{ menuItem.title }}</p>
  </li>
</template>
