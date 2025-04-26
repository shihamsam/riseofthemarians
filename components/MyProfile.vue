<template>
  <div
    class="w-full max-w-sm bg-white border border-gray-200 rounded-lg shadow-sm dark:bg-gray-800 dark:border-gray-700"
  >
    <div class="text-xl text-white bg-[#253b9b] p-2 block rounded-t-lg">
      <slot name="title">Role</slot>
    </div>
    <div class="flex flex-col items-center p-5 gap-2">
      <img
        v-if="profileImage"
        class="w-32 h-32 rounded-full shadow-lg object-cover start-0"
        :src="`${profileImage}`"
        alt="Bonnie image"
      />

      <div
        v-if="!profileImage"
        class="relative w-32 h-32 overflow-hidden bg-gray-100 rounded-full dark:bg-gray-600"
      >
        <svg
          class="absolute w-60 h-60 text-gray-400 -left-2.5"
          fill="currentColor"
          viewBox="0 0 32 32"
          xmlns="http://www.w3.org/2000/svg"
        >
          <path
            fill-rule="evenodd"
            d="M10 9a3 3 0 100-6 3 3 0 000 6zm-7 9a7 7 0 1114 0H3z"
            clip-rule="evenodd"
          ></path>
        </svg>
      </div>

      <h5 class="mb-1 text-xl font-medium text-gray-900 dark:text-white">
        <slot name="name">Bonnie Green</slot>
      </h5>

      <div>
        <slot name="designation"></slot>
      </div>

      <span class="text-md text-gray-500 dark:text-gray-400">
        <slot name="phone"></slot>
      </span>
    </div>
  </div>
</template>

<script setup lang="ts">
import { defineProps } from "vue";

const props = defineProps({
  profileImage: { type: String, required: false },
});
</script>
