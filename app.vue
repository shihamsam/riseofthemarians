<template>
  <NuxtLayout />
</template>
<script setup lang="ts">
import { initFlowbite } from "flowbite";
import { onMounted } from "vue";
import { useFlowbite } from "~/composables/useFlowbite";

useSeoMeta({
  title: "P/FBMV - Grade 6 - 2025",
  ogTitle: "P/FBMV - Grade 6 - 2025",
  description:
    "This is the official website of P/FBMV - Grade 6 - 2025. We aim to provide the best education for our students.",
  ogDescription:
    "This is the official website of P/FBMV - Grade 6 - 2025. We aim to provide the best education for our students.",
  ogImage: "/images/logo.jpg",
  twitterCard: "summary_large_image",
});

// initialize components based on data attribute selectors
onMounted(() => {
  useFlowbite(() => {
    initFlowbite();
  });
});
</script>
