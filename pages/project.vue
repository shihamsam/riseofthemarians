<template>
  <main>
    <HeroTitle>
      <template #title>Project Estimations</template>
      <template #subtitle>
        Support our mission to make St.Mary's College a better place for our
        students.
      </template>
    </HeroTitle>

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
                  id="project01-tab"
                  data-tabs-target="#project01"
                  type="button"
                  role="tab"
                  aria-controls="project01"
                  aria-selected="true"
                >
                  01. Assembly Area
                </button>
              </li>
              <li class="me-2" role="presentation">
                <button
                  class="inline-block p-4 border-b-2 rounded-t-lg hover:text-gray-600 hover:border-gray-300 dark:hover:text-gray-300"
                  id="project02-tab"
                  data-tabs-target="#project02"
                  type="button"
                  role="tab"
                  aria-controls="project02"
                  aria-selected="false"
                >
                  02. School Ground
                </button>
              </li>
              <li class="me-2" role="presentation">
                <button
                  class="inline-block p-4 border-b-2 rounded-t-lg"
                  id="project03-tab"
                  data-tabs-target="#project03"
                  type="button"
                  role="tab"
                  aria-controls="project03"
                  aria-selected="false"
                >
                  03. To be Decided
                </button>
              </li>
            </ul>
          </div>
          <div id="default-tab-content">
            <div
              class="hidden p-4 rounded-lg bg-gray-50 dark:bg-gray-800"
              id="project01"
              role="tabpanel"
              aria-labelledby="project01-tab"
            >
              <div class="bg-white p-6 rounded-lg shadow-lg">
                <h3 class="text-xl font-semibold mb-4">Assembly Area</h3>
                <p class="text-gray-600 mb-4">
                  Estimation of expences Project No.1
                </p>

                <ProjectEstimateGallery
                  :folderName="proj01Estimates"
                  :itemCount="4"
                />
              </div>
            </div>
            <div
              class="hidden p-4 rounded-lg bg-gray-50 dark:bg-gray-800"
              id="project02"
              role="tabpanel"
              aria-labelledby="project02-tab"
            >
              <div class="bg-white p-6 rounded-lg shadow-lg">
                <h3 class="text-xl font-semibold mb-4">School Ground</h3>
                <p class="text-gray-600 mb-4">
                  Estimation of expences Project No.2
                </p>
              </div>
            </div>
            <div
              class="p-4 rounded-lg bg-gray-50 dark:bg-gray-800"
              id="project03"
              role="tabpanel"
              aria-labelledby="project03-tab"
            >
              <div class="bg-white p-6 rounded-lg shadow-lg">
                <h3 class="text-xl font-semibold mb-4">To be Decided</h3>
                <p class="text-gray-600 mb-4">To be Decided</p>
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
import Project01EstimateGallery from "~/components/ProjectEstimateGallery.vue";
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
