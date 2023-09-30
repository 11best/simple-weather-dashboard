<script setup lang="ts">
import Header from "./components/Header.vue";
import Sidebar from "./components/Sidebar/Sidebar.vue";
import ImageContainer from "./components/ImageContainer.vue";
import GraphContainer from "./components/GraphContainer.vue";
import IndexLevel from "./components/IndexLevel.vue";
</script>

<template>
  <div class="min-h-screen flex flex-col">
    <Header />
    <div class="relative flex flex-grow">
      <Sidebar />
      <main class="bg-pink-500 ml-64 flex-1">
        <div class="grid grid-cols-5 gap-x-4 p-4 h-full">
          <div class="w-full col-span-3 flex flex-col gap-4">
            <div class="h-3/6"><ImageContainer /></div>
            <div class="h-2/6"><GraphContainer /></div>
            <div class="flex items-center"><IndexLevel /></div>
          </div>
          <div class="w-full bg-green-300 col-span-2">ccc</div>
        </div>
      </main>
    </div>
  </div>
</template>
