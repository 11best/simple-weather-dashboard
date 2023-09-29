<script setup lang="ts">
import CollapseItem from "./CollapseItem.vue";

defineProps<{
  menuInfo: { mainMenuTitle: string; menuItem: { title: string }[] };
}>();
</script>

<template>
  <div
    id="sidebar-main-menu"
    class="rounded-full cursor-pointer hover:bg-slate-300 px-4 py-2 flex justify-between"
  >
    <p>{{ menuInfo.mainMenuTitle }}</p>
    <p>V</p>
  </div>
  <ul>
    <CollapseItem v-for="menuItem in menuInfo.menuItem" :menu-item="menuItem" />
  </ul>
</template>
