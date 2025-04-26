<script setup lang="ts">
import MyGallery from "~/components/ProjectProposalGallery.vue";
</script>

<template>
  <main>
    <HeroTitle>
      <template #title>Memories</template>
      <template #subtitle>
        Support our mission to make St.Mary's College a better place for our
        students.</template
      >
    </HeroTitle>

    <!-- In Progress renovation Section -->
    <section class="py-10 flex flex-col items-center">
      <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
        <h2 class="text-3xl font-bold text-center mb-12 text-gray-700">
          Sharing the History
        </h2>
        <ImageGallery :itemCount="10" />
      </div>
    </section>
  </main>
</template>
