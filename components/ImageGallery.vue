<template>
  <div class="grid grid-cols-1 md:grid-cols-2 gap-4">
    <div
      v-for="slide in reverseRange"
      :key="slide"
      class="border border-gray-300 rounded-lg shadow-md overflow-hidden"
    >
      <img
        class="h-auto max-w-full rounded-lg"
        :src="`../images/${folderName}/${normalizeSlideNumber(slide)}.jpg`"
        alt=""
      />
    </div>
  </div>
</template>

<script setup lang="ts">
import { ref } from "vue";

const normalizeSlideNumber = (number: number) => {
  return number < 10 ? `0${number}` : number;
};
const props = defineProps({
  folderName: {
    type: String,
    default: "progress",
  },
  itemCount: {
    type: Number,
    default: 4,
  },
});

// reverse the range
const reverseRange = computed(() => {
  return Array.from({ length: props.itemCount }, (_, i) => 1 + i).reverse();
});
</script>
