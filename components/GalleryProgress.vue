<template>
  <div class="grid grid-cols-2 md:grid-cols-3 gap-4">
    <div v-for="slide in slides" :key="slide.id">
      <img
        class="h-auto max-w-full rounded-lg"
        :src="`../images/progress/${slide.image}`"
        alt=""
      />
    </div>
  </div>
</template>

<script setup>
import { ref } from "vue";

const slides = ref([
  {
    id: 0,
    image: "001_categorization_01.jpeg",
  },
  {
    id: 1,
    image: "001_categorization_02.jpeg",
  },
  {
    id: 2,
    image: "001_categorization_03.jpeg",
  },
  {
    id: 3,
    image: "002_welding_01.jpeg",
  },
  {
    id: 4,
    image: "002_welding_02.jpeg",
  },
  {
    id: 5,
    image: "003_painting_01.jpeg",
  },
  {
    id: 6,
    image: "003_painting_02.jpeg",
  },
  {
    id: 7,
    image: "003_painting_03.jpeg",
  },
  {
    id: 8,
    image: "003_painting_03_1.jpeg",
  },
  {
    id: 9,
    image: "003_painting_04.jpeg",
  },
  {
    id: 10,
    image: "003_painting_05.jpeg",
  },
  {
    id: 11,
    image: "003_painting_06.jpeg",
  },
  {
    id: 12,
    image: "003_painting_07.jpeg",
  },
  {
    id: 13,
    image: "003_painting_08.jpeg",
  },
  {
    id: 14,
    image: "003_painting_09_with_label.jpeg",
  },
  {
    id: 15,
    image: "WhatsApp Image 2025-02-04 at 10.54.32 AM (1).jpeg",
  },
]);
</script>
