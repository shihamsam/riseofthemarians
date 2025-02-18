<template>
  <main>
    <section class="relative bg-green-900 text-white pt-32 pb-8">
      <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8 text-center">
        <h1 class="text-4xl font-bold mb-4">Project Estimations</h1>
        <p class="text-xl mb-1">
          Support our mission to renovate and improve our school facilities
        </p>
      </div>
    </section>

    <!-- PDF Showcase Section -->
    <section class="py-10 bg-gray-100">
      <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
        <div>
          <div class="mb-4 border-b border-gray-200 dark:border-gray-700">
            <ul
              class="flex flex-wrap -mb-px text-sm font-medium text-center"
              id="default-tab"
              data-tabs-toggle="#default-tab-content"
              role="tablist"
            >
              <li class="me-2" role="presentation">
                <button
                  class="inline-block p-4 border-b-2 rounded-t-lg hover:text-gray-600 hover:border-gray-300 dark:hover:text-gray-300"
                  id="dashboard-tab"
                  data-tabs-target="#dashboard"
                  type="button"
                  role="tab"
                  aria-controls="dashboard"
                  aria-selected="true"
                >
                  Class Rooms and Furniture
                </button>
              </li>
              <li class="me-2" role="presentation">
                <button
                  class="inline-block p-4 border-b-2 rounded-t-lg hover:text-gray-600 hover:border-gray-300 dark:hover:text-gray-300"
                  id="settings-tab"
                  data-tabs-target="#settings"
                  type="button"
                  role="tab"
                  aria-controls="settings"
                  aria-selected="false"
                >
                  Sanitation Facilities
                </button>
              </li>
              <li class="me-2" role="presentation">
                <button
                  class="inline-block p-4 border-b-2 rounded-t-lg"
                  id="profile-tab"
                  data-tabs-target="#profile"
                  type="button"
                  role="tab"
                  aria-controls="profile"
                  aria-selected="false"
                >
                  Estimate for Road
                </button>
              </li>
            </ul>
          </div>
          <div id="default-tab-content">
            <div
              class="p-4 rounded-lg bg-gray-50 dark:bg-gray-800"
              id="profile"
              role="tabpanel"
              aria-labelledby="profile-tab"
            >
              <div class="bg-white p-6 rounded-lg shadow-lg">
                <h3 class="text-xl font-semibold mb-4">
                  Estimation Documents for Road
                </h3>
                <p class="text-gray-600 mb-4">
                  Detailed Estimation outlining the expenses for renovation.
                </p>
                <embed
                  :src="roadEstimation"
                  type="application/pdf"
                  class="w-full min-h-[500px]"
                />
              </div>
            </div>
            <div
              class="hidden p-4 rounded-lg bg-gray-50 dark:bg-gray-800"
              id="dashboard"
              role="tabpanel"
              aria-labelledby="dashboard-tab"
            >
              <div class="bg-white p-6 rounded-lg shadow-lg">
                <h3 class="text-xl font-semibold mb-4">
                  Class Rooms and Furniture (Page 2 & 3)
                </h3>
                <p class="text-gray-600 mb-4">
                  Detailed Estimation outlining the expenses for renovation.
                </p>
                <embed
                  :src="classRoomsEstimation"
                  type="application/pdf"
                  class="w-full min-h-[500px]"
                />
              </div>
            </div>
            <div
              class="hidden p-4 rounded-lg bg-gray-50 dark:bg-gray-800"
              id="settings"
              role="tabpanel"
              aria-labelledby="settings-tab"
            >
              <div class="bg-white p-6 rounded-lg shadow-lg">
                <h3 class="text-xl font-semibold mb-4">
                  Sanitation Facilities (Page 1)
                </h3>
                <p class="text-gray-600 mb-4">
                  Detailed Estimation outlining the renovation for Sanitation
                  facilities.
                </p>
                <embed
                  :src="sanitationEstimation"
                  type="application/pdf"
                  class="w-full min-h-[500px]"
                />
              </div>
            </div>
          </div>
        </div>
      </div>
    </section>
  </main>
</template>

<script setup>
const roadEstimation = "/docs/001_estimation.pdf";
const classRoomsEstimation = "/docs/002_estimation.pdf";
const sanitationEstimation = "/docs/002_estimation.pdf";

const route = useRoute();
import { useFlowbite } from "~/composables/useFlowbite";

onMounted(() => {
  useFlowbite(() => {
    initFlowbite();
  });
});
</script>

<style scoped>
/* Add custom styles for the tabs if needed */
</style>
