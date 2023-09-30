<script setup lang="ts">
defineProps<{
  data: any;
}>();
</script>

<template>
  <div class="bg-white opacity-80 w-full h-full rounded-lg">
    <div class="bg-green-200 rounded-full w-full flex">
      <div
        class="w-12 h-12 rounded-full bg-green-500 flex items-center justify-center"
      >
        {{ data.icon }}
      </div>
      <span
        v-html="data.title"
        class="flex items-center ml-2 font-bold text-xl"
      ></span>
    </div>
    <div class="p-2">
      <div class="flex justify-center relative">
        <div class="font-bold text-4xl mt-1">{{ data.value }}</div>
        <div
          v-html="data.unit"
          class="text-xs absolute top-[-7px] left-2/3"
        ></div>
      </div>
      <div class="text-center text-xs mt-2">{{ data.detail }}</div>
    </div>
  </div>
</template>
