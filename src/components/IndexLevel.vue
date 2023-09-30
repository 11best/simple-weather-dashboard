<script setup lang="ts">
const mockLevel = [
  {
    title: "Good",
    detail: "0 to 50",
    icon: "😀",
    color: "green",
  },
  {
    title: "Moderate",
    detail: "51 to 100",
    icon: "😀",
    color: "yellow",
  },
  {
    title: "Unhealthy",
    detail: "101 to 150",
    icon: "😀",
    color: "orange",
  },
  {
    title: "Unhealthy",
    detail: "151 to 200",
    icon: "😀",
    color: "red",
  },
  {
    title: "Very Unhealthy",
    detail: "201 to 300",
    icon: "😀",
    color: "purple",
  },
  {
    title: "Very Unhealthy",
    detail: "301 to 500",
    icon: "😀",
    color: "brown",
  },
];
</script>

<template>
  <div class="bg-white opacity-70 w-full h-20 rounded-lg flex">
    <div class="bg-green-300 p-2 w-24 text-sm rounded-lg">
      title title title title
    </div>
    <div class="w-full flex justify-evenly">
      <div
        v-for="item in mockLevel"
        class="text-sm flex overflow-auto items-center"
      >
        <div
          class="flex items-center justify-center w-8 h-8 rounded-full"
          :style="{ backgroundColor: item.color }"
        >
          {{ item.icon }}
        </div>
        <div :style="{ color: item.color }">
          <p>
            {{ item.title }}
          </p>
          <p>
            {{ item.detail }}
          </p>
        </div>
      </div>
    </div>
  </div>
</template>
