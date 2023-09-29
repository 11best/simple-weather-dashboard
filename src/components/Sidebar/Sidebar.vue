<script setup lang="ts">
import Collapse from "./Collapse.vue";

const mockSidebarItems = [
  {
    mainMenuTitle: "Main menu 1",
    menuItem: [
      {
        title: "menu 1 item 1",
      },
      {
        title: "menu 1 item 2",
      },
    ],
  },
  {
    mainMenuTitle: "Main menu 2",
    menuItem: [
      {
        title: "menu 2 item 1",
      },
      {
        title: "menu 2 item 2",
      },
      {
        title: "menu 2 item 2",
      },
    ],
  },
];
</script>

<template>
  <nav id="sidebar" class="w-72 min-h-screen fixed">
    <Collapse v-for="item in mockSidebarItems" :menu-info="item" />
  </nav>
</template>
