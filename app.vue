<template>
  <NuxtLayout />
</template>
<script setup lang="ts">
import { initFlowbite } from "flowbite";
import { onMounted } from "vue";
import { useFlowbite } from "~/composables/useFlowbite";

useSeoMeta({
  title: "Rise of the Marians - Hambantota",
  ogTitle: "Rise of the Marians - Hambantota",
  description:
    "This is the official website of Rise of the Marians - Hambantota. We aim to provide the best education and facilities for our students.",
  ogDescription:
    "This is the official website of Rise of the Marians - Hambantota. We aim to provide the best education and facilities for our students.",
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
