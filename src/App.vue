<script setup lang="ts">
import Header from "./components/Header.vue";
import Sidebar from "./components/Sidebar/Sidebar.vue";
</script>

<template>
  <div class="min-h-screen flex flex-col">
    <Header />
    <div class="relative flex flex-grow">
      <Sidebar />
      <main class="bg-pink-500 ml-72 flex-1">
        <div class="grid grid-cols-5 p-4 h-full">
          <div class="w-full bg-orange-300 col-span-3">ddd</div>
          <div class="w-full bg-green-300 col-span-2">ccc</div>
        </div>
      </main>
    </div>
  </div>
</template>
