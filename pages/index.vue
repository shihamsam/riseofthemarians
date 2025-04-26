<script setup lang="ts"></script>

<template>
  <main>
    <!-- Hero Section -->
    <!-- <section
      class="relative text-white py-32 bg-[url(../images/hero/hero_image.png)] bg-no-repeat bg-cover"
    > -->
    <section
      class="flex flex-col align-middle items-center text-white mt-24 bg-white bg-no-repeat bg-cover"
    >
      <img src="/images/hero/riseofthemarians-backdrop.jpg" alt="logo" />

      <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8 text-center">
        <h1
          class="hidden text-4xl mt-10 font-bold mb-4 drop-shadow-lg items-center"
        >
          Thriving Together for a Promising Tomorrow
        </h1>
      </div>
    </section>

    <!-- Goals Section -->
    <!-- <section class="py-10">
      <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
        <h2 class="text-3xl font-bold text-center mb-12 text-gray-700">
          Our Goals for a Better Learning Environment
        </h2>
        <div class="grid grid-cols-1 md:grid-cols-3 gap-8">
          <MyCard>
            <template #title> Classroom Complex with Furniture</template>
            Renovating Grade 6 classrooms and furniture to create a better
            learning environment
          </MyCard>
          <MyCard>
            <template #title> Sanitation Facilities</template>
            Upgrading toilets and washing facilities
          </MyCard>
          <MyCard>
            <template #title> Access Road</template>
            Improving accessibility for students and staff
          </MyCard>
        </div>
      </div>
    </section> -->

    <!-- Class Rooms Section -->
    <section class="py-10 flex flex-col items-center">
      <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
        <h2 class="text-3xl font-bold text-center mb-12 text-gray-600">
          Rise of the Marians - Project Proposals
        </h2>
        <ProjectProposalGallery />
      </div>
    </section>
  </main>
</template>
