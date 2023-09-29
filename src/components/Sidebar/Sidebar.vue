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
  <nav
    id="sidebar"
    class="w-72 px-4 absolute h-full flex flex-col justify-between"
  >
    <div>
      <Collapse v-for="item in mockSidebarItems" :menu-info="item" />
    </div>
    <button
      class="bg-green-500 flex justify-center items-center w-full rounded-full px-4 py-2 mb-8"
    >
      <div class="mr-2">icon</div>
      Log out
    </button>
  </nav>
</template>
