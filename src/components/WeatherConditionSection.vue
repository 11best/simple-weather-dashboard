<script setup lang="ts">
import TextContainer from "./TextContainer.vue";
import Card from "./Card.vue";

const mockWeatherConditions = [
  {
    title: "Temperature",
    icon: "☁️",
    value: "26.3",
    unit: "°C",
  },
  {
    title: "Relative Humidity",
    icon: "💧",
    value: "83",
    unit: "%",
  },
  {
    title: "Wind Speed",
    icon: "🌬️",
    value: "0.3",
    unit: "m/s",
  },
];
</script>

<template>
  <TextContainer title="Real Time Weather Conditions" />
  <div class="grid grid-cols-3 gap-4 mt-2">
    <Card v-for="item in mockWeatherConditions" :data="item" />
  </div>
</template>
