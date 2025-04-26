<template>
  <section class="relative bg-[#192768] text-white pt-36 pb-8">
    <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8 text-center">
      <h1 class="text-2xl font-bold mb-4">
        <slot name="title"> My Title </slot>
      </h1>
      <p class="text-xl mb-1">
        <slot name="subtitle"> My Sub Title </slot>
      </p>
    </div>
  </section>
</template>

<script setup lang="ts"></script>
