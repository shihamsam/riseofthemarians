<script setup lang="ts">
definePageMeta({
  layout: "underconstruction",
});
</script>

<template>
  <div
    class="min-h-screen bg-gray-900 flex flex-col items-center justify-center relative px-4"
  >
    <!-- <div
      class="absolute top-0 left-0 w-full h-full bg-contain bg-no-repeat opacity-100 lg:hidden bg-white"
      style="
        background-image: url('/underconstruction/riseofthemarians-backdrop.jpg');
      "
    > -->
    <div
      class="absolute top-0 left-0 w-full h-full bg-contain bg-no-repeat opacity-100 xl:hidden bg-white"
    >
      <img
        src="/underconstruction/riseofthemarians-backdrop.jpg"
        layout="fill"
      />
      <h1
        class="text-5xl md:text-5xl text-gray-500 text-center font-bold mb-8 z-10 pt-16"
      >
        Coming Soon
      </h1>
      <p class="text-gray-600 text-xl text-center p-10 md:p-6 md:text-2xl">
        We're working hard to bring you something amazing. Stay tuned!
      </p>
    </div>

    <div
      class="absolute top-0 left-0 w-full h-full bg-cover bg-center opacity-100 max-xl:hidden"
      style="
        background-image: url('/underconstruction/riseofthemarians-backdrop.jpg');
      "
    ></div>
  </div>
</template>
