<template>
  <div class="grid grid-cols-2 md:grid-cols-2 gap-4">
    <div
      v-for="slide in 13"
      :key="slide.id"
      class="border border-gray-200 rounded-lg shadow-md overflow-hidden"
    >
      <img
        class="h-auto max-w-full rounded-lg"
        :src="`../images/projects/proposals/${normalizeSlideNumber(slide)}.jpg`"
        alt=""
      />
    </div>
  </div>
</template>

<script setup>
import { ref } from "vue";

const normalizeSlideNumber = (number) => {
  return number < 10 ? `0${number}` : number;
};
</script>
