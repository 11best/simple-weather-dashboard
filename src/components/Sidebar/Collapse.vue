<script setup lang="ts">
import CollapseItem from "./CollapseItem.vue";
import { ref } from "vue";

const isExpanded = ref(false);

function setExpand() {
  isExpanded.value = !isExpanded.value;
}

defineProps<{
  menuInfo: { mainMenuTitle: string; menuItem: { title: string }[] };
}>();
</script>

<template>
  <div
    id="sidebar-main-menu"
    @click="setExpand"
    class="rounded-full cursor-pointer hover:bg-green-300 px-4 py-2 flex justify-between"
    :class="[{ 'bg-green-400': isExpanded }]"
  >
    <p>{{ menuInfo.mainMenuTitle }}</p>
    <p :class="[{ 'rotate-180': isExpanded }]">V</p>
  </div>
  <ul :class="[{ hidden: !isExpanded }]">
    <CollapseItem v-for="menuItem in menuInfo.menuItem" :menu-item="menuItem" />
  </ul>
</template>
