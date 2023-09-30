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
</script>

<template>
  <TextContainer title="Real Air Pollution" />
  <div class="grid grid-cols-3 gap-2 mt-2">
    <CardWithLabel v-for="item in mockWeatherConditions" :data="item" />
  </div>
</template>
