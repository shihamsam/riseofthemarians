<template>
  <div class="grid grid-cols-2 md:grid-cols-3 gap-4">
    <div v-for="slide in slides" :key="slide.id">
      <img
        class="h-auto max-w-full rounded-lg"
        :src="`../images/beforechange/${slide.image}`"
        alt=""
      />
    </div>
  </div>
</template>

<script setup>
import { ref } from "vue";

const slides = ref([
  {
    image: "002_toilet_door_1.jpeg",
    id: 1,
  },
  {
    image: "002_toilet_inside_1.jpeg",
    id: 2,
  },
  {
    image: "002_toilet_inside_2.jpeg",
    id: 3,
  },
  {
    image: "002_toilet_outside_1.jpeg",
    id: 4,
  },

  {
    image: "002_toilet_outside_3.jpeg",
    id: 5,
  },
  {
    image: "002_toilet_outside_4.jpeg",
    id: 6,
  },
  {
    image: "002_toilet_outside_tank_1.jpeg",
    id: 7,
  },
  {
    image: "003_road_1.jpeg",
    id: 8,
  },
  {
    image: "003_road_2.jpeg",
    id: 9,
  },
  {
    image: "004_wall_1.jpeg",
    id: 10,
  },
  {
    image: "004_wall_2.jpeg",
    id: 11,
  },
  {
    image: "004_wall_3.jpeg",
    id: 12,
  },
  {
    image: "004_wall_4.jpeg",
    id: 13,
  },
  {
    image: "004_wall_5.jpeg",
    id: 14,
  },
  {
    image: "001_first_meeting.jpeg",
    id: 15,
  },
  {
    image: "002_toilet_outside_2.jpeg",
    id: 16,
  },
]);
</script>
