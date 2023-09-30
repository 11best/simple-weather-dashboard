<script setup lang="ts">
import Header from "./components/Header.vue";
import Sidebar from "./components/Sidebar/Sidebar.vue";
import ImageContainer from "./components/ImageContainer.vue";
import GraphContainer from "./components/GraphContainer.vue";
import IndexLevel from "./components/IndexLevel.vue";
import AqiSummary from "./components/AqiSummary.vue";
import WeatherConditionSection from "./components/WeatherConditionSection.vue";
import PollutionSection from "./components/PollutionSection.vue";
</script>

<template>
  <div class="min-h-screen flex flex-col">
    <Header />
    <div class="relative flex flex-grow">
      <Sidebar />
      <main class="ml-64 flex-1 bg-[url(https://picsum.photos/id/29/1280/720)]">
        <div class="grid grid-cols-5 gap-x-4 p-8 h-full">
          <div id="left-section" class="w-full col-span-3 flex flex-col gap-4">
            <div class="h-3/6"><ImageContainer /></div>
            <div class="h-3/6"><GraphContainer /></div>
            <div class="flex items-center"><IndexLevel /></div>
          </div>
          <div id="right-section" class="w-full col-span-2">
            <AqiSummary />
            <div class="my-4">
              <WeatherConditionSection />
            </div>
            <div>
              <PollutionSection />
            </div>
          </div>
        </div>
      </main>
    </div>
  </div>
</template>
