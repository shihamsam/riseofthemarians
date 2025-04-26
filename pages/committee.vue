<template>
  <main>
    <HeroTitle>
      <template #title>Our Committee Members</template>
      <template #subtitle>
        Support our mission to make St.Mary's College a better place for our
        students.</template
      >
    </HeroTitle>
    <section class="relative pt-8 pb-8">
      <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8 text-center">
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
                  Rise of the Marians Committee
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
                  School Development Committee (SDC)
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
                  Past Pupils Association (PPA)
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
                <h3 class="text-xl font-semibold mb-6">
                  Past Pupils Association (PPA)
                </h3>
                <div class="grid lg:grid-cols-4 md:grid-cols-3 gap-5">
                  <MyProfile
                    v-for="profile in ppaMembers"
                    :key="profile.name"
                    :profile-image="profile.profileImage"
                  >
                    <template #title>{{ profile.title }}</template>
                    <template #name>{{ profile.name }}</template>
                    <template #phone>📞 {{ profile.phone }}</template>

                    <template #designation>
                      <div
                        class="text-[1rem] font-normal text-gray-500 dark:text-gray-400 block"
                      >
                        {{ profile.designation }}
                      </div>
                      <div
                        class="text-[0.8rem] font-normal text-gray-500 dark:text-gray-400"
                      >
                        {{ profile.company }}
                      </div>
                    </template>
                  </MyProfile>
                </div>
              </div>
            </div>
            <div
              class="hidden p-4 rounded-lg bg-gray-50 dark:bg-gray-800"
              id="dashboard"
              role="tabpanel"
              aria-labelledby="dashboard-tab"
            >
              <div class="bg-white p-6 rounded-lg shadow-lg">
                <h3 class="text-xl font-semibold mb-6">
                  Rise of the Marians Committee
                </h3>

                <div class="grid lg:grid-cols-4 md:grid-cols-3 gap-5">
                  <MyProfile
                    v-for="profile in riseOfTheMariansCommitteeMembers"
                    :key="profile.name"
                    :profile-image="profile.profileImage"
                  >
                    <template #title>{{ profile.title }}</template>
                    <template #name>{{ profile.name }}</template>
                    <template #phone>📞 {{ profile.phone }}</template>

                    <template #designation>
                      <div
                        class="text-[1rem] font-normal text-gray-500 dark:text-gray-400 block"
                      >
                        {{ profile.designation }}
                      </div>
                      <div
                        class="text-[0.8rem] font-normal text-gray-500 dark:text-gray-400"
                      >
                        {{ profile.company }}
                      </div>
                    </template>
                  </MyProfile>
                </div>
              </div>
            </div>
            <div
              class="hidden p-4 rounded-lg bg-gray-50 dark:bg-gray-800"
              id="settings"
              role="tabpanel"
              aria-labelledby="settings-tab"
            >
              <div class="bg-white p-6 rounded-lg shadow-lg">
                <h3 class="text-xl font-semibold mb-6">
                  School Development Committee (SDC)
                </h3>

                <div class="grid lg:grid-cols-4 md:grid-cols-3 gap-5">
                  <MyProfile
                    v-for="profile in sdcMembers"
                    :key="profile.name"
                    :profile-image="profile.profileImage"
                  >
                    <template #title>{{ profile.title }}</template>
                    <template #name>{{ profile.name }}</template>
                    <template #phone>📞 {{ profile.phone }}</template>

                    <template #designation>
                      <div
                        class="text-[1rem] font-normal text-gray-500 dark:text-gray-400 block"
                      >
                        {{ profile.designation }}
                      </div>
                      <div
                        class="text-[0.8rem] font-normal text-gray-500 dark:text-gray-400"
                      >
                        {{ profile.company }}
                      </div>
                    </template>
                  </MyProfile>
                </div>
              </div>
            </div>
          </div>
        </div>
      </div>
    </section>
  </main>
</template>

<script setup lang="ts">
const roadEstimation = "/docs/001_estimation.pdf";
const classRoomsEstimation = "/docs/002_estimation.pdf";
const sanitationEstimation = "/docs/002_estimation.pdf";

const route = useRoute();
import { initFlowbite } from "flowbite";
import { useFlowbite } from "~/composables/useFlowbite";

onMounted(() => {
  useFlowbite(() => {
    initFlowbite();
  });
});

const riseOfTheMariansCommitteeMembers = [
  {
    title: "President",
    name: "NAME",
    phone: "+94 77 777 7777",
    designation: "Designation",
    company: "Organization",
    profileImage: "",
    email: "",
  },
  {
    title: "Treasurer",
    name: "NAME",
    phone: "+94 77 777 7777",
    designation: "Designation",
    company: "Organization",
    profileImage: "",
    email: "",
  },

  {
    title: "Secretary",
    name: "NAME",
    phone: "+94 77 777 7777",
    designation: "Designation",
    company: "Organization",
    profileImage: "",
    email: "",
  },
  {
    title: "Member 1",
    name: "NAME",
    phone: "+94 77 777 7777",
    designation: "Designation",
    company: "Organization",
    profileImage: "",
    email: "",
  },
];

const ppaMembers = [
  {
    title: "President",
    name: "NAME",
    phone: "+94 XX XXX XXXX",
    designation: "Designation",
    company: "Organization",
    profileImage: "",
    email: "",
  },
  {
    title: "Treasurer",
    name: "NAME",
    phone: "+94 XX XXX XXXX",
    designation: "Designation",
    company: "Organization",
    profileImage: "",
    email: "",
  },
  {
    title: "Secretary",
    name: "NAME",
    phone: "+94 XX XXX XXXX",
    designation: "Designation",
    company: "Organization",
    profileImage: "",
    email: "",
  },
  {
    title: "Member 1",
    name: "NAME",
    phone: "+94 77 777 7777",
    designation: "Designation",
    company: "Organization",
    profileImage: "",
    email: "",
  },
];

const sdcMembers = [
  {
    title: "President",
    name: "NAME",
    phone: "+94 XX XXX XXXX",
    designation: "Designation",
    company: "Organization",
    profileImage: "",
    email: "",
  },
  {
    title: "Treasurer",
    name: "NAME",
    phone: "+94 XX XXX XXXX",
    designation: "Designation",
    company: "Organization",
    profileImage: "",
    email: "",
  },
  {
    title: "Secretary",
    name: "NAME",
    phone: "+94 XX XXX XXXX",
    designation: "Designation",
    company: "Organization",
    profileImage: "",
    email: "",
  },
  {
    title: "Member 1",
    name: "NAME",
    phone: "+94 77 777 7777",
    designation: "Designation",
    company: "Organization",
    profileImage: "",
    email: "",
  },
];
</script>
