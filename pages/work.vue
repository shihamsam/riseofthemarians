<script setup lang="ts">
import MyGallery from "~/components/GalleryBefore.vue";
</script>

<template>
  <main>
    <section class="relative bg-green-900 text-white pt-32 pb-8">
      <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8 text-center">
        <h1 class="text-4xl font-bold mb-4">Walking the Talk</h1>
        <p class="text-xl mb-1">
          Support our mission to renovate and improve our school facilities
        </p>
      </div>
    </section>

    <!-- In Progress renovation Section -->
    <section class="py-10 flex flex-col items-center">
      <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
        <h2 class="text-3xl font-bold text-center mb-12 text-gray-700">
          Pictures of Work In Progress
        </h2>
        <GalleryProgress />
      </div>
    </section>
  </main>
</template>
