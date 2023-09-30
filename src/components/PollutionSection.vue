<script setup lang="ts">
import TextContainer from "./TextContainer.vue";
import CardWithLabel from "./CardWithLabel.vue";

const mockWeatherConditions = [
  {
    title: "PM 2.5",
    icon: "☁️",
    value: "20",
    unit: "pg./m<sup>2</sup>",
    detail: "Although camelCase keys are recommended",
  },
  {
    title: "PM 10",
    icon: "💧",
    value: "55",
    unit: "pg./m<sup>2</sup>",
    detail: "It is often a good idea to bind to a style object directly",
  },
  {
    title: "O<sub>3</sub>",
    icon: "🌬️",
    value: "12",
    unit: "ppm",
    detail: "papuan cute",
  },
  {
    title: "NO<sub>2</sub>",
    icon: "🌬️",
    value: "26",
    unit: "ppm",
    detail: "papuan cute",
  },
  {
    title: "CO<sub>2</sub>",
    icon: "🌬️",
    value: "318",
    unit: "ppm",
    detail: "papuan cute",
  },
  {
    title: "CH<sub>4</sub>",
    icon: "🌬️",
    value: "0.3",
    unit: "%LEL",
    detail: "papuan cute",
  },
];

const mockLevel = [
  { name: "normal", color: "green" },
  { name: "crisis", color: "orange" },
  { name: "hazard", color: "red" },
];
</script>

<template>
  <TextContainer title="Real Air Pollution" />
  <div class="grid grid-cols-3 gap-2 mt-2">
    <CardWithLabel v-for="item in mockWeatherConditions" :data="item" />
  </div>
  <div
    class="w-full bg-white opacity-70 rounded-full flex justify-evenly p-2 mt-4"
  >
    <div v-for="level in mockLevel" class="flex items-center">
      <div
        class="w-6 h-3 rounded-full"
        :style="{ backgroundColor: level.color }"
      ></div>
      <p class="text-xs ml-2">{{ level.name }}</p>
    </div>
  </div>
</template>
