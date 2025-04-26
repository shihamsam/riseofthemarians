<template>
  <div class="grid grid-cols-1 md:grid-cols-1 gap-4">
    <div
      v-for="slide in itemCount"
      :key="slide"
      class="border border-gray-200 rounded-lg shadow-md overflow-hidden"
    >
      <img
        class="h-auto max-w-full rounded-lg"
        :src="`../images/projects/${folderName}/${normalizeSlideNumber(
          slide
        )}.jpg`"
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

defineProps({
  folderName: {
    type: String,
    default: "proj01Estimates",
  },
  itemCount: {
    type: Number,
    default: 4,
  },
});
</script>
