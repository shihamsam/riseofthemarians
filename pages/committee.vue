<template>
  <main>
    <section class="relative bg-green-900 text-white pt-32 pb-8">
      <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8 text-center">
        <h1 class="text-4xl font-bold mb-4">
          Contact Us for your
          <span class="text-yellow-400 animate-pulse">Donations</span>
        </h1>

        <p class="text-xl mb-1">
          Support our mission to renovate and improve our school facilities
        </p>
      </div>
    </section>
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
                  Grade 6 - Building Committee
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
                  Grade 6 - Building Committee
                </h3>

                <div class="grid lg:grid-cols-4 md:grid-cols-3 gap-5">
                  <MyProfile
                    v-for="profile in grade6CommitteeMembers"
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
import { useFlowbite } from "~/composables/useFlowbite";

onMounted(() => {
  useFlowbite(() => {
    initFlowbite();
  });
});

const grade6CommitteeMembers = [
  {
    title: "President",
    name: "Mr. Aashiq",
    phone: "+94 72 918 2166",
    designation: "Designation",
    company: "Organization",
    profileImage: "",
    email: "",
  },
  {
    title: "Treasurer",
    name: "SFM RAMEEZ",
    phone: "+94 71 720 2040",
    designation: "Managing Director",
    company: "Mega Group of Companies",
    profileImage: "/images/profiles/rameez-profile.png",
    email: "",
  },
  {
    title: "Secretary",
    name: "MJ Mohamed Naleem",
    phone: "+94 71 920 0006",
    designation: "Building Contractor",
    company: "Faargo Construction (Pvt) Ltd",
    profileImage: "",
    email: "fargopx@gmail.com",
  },
  {
    title: "Member",
    name: "Mr. Gadafi",
    phone: "+94 74 243 4352",
    designation: "Designation",
    company: "Organization",
    profileImage: "",
    email: "",
  },
  {
    title: "Member",
    name: "Mr. Jaleel",
    phone: "+94 77 345 7930",
    designation: "Designation",
    company: "Organization",
    profileImage: "",
    email: "",
  },
  {
    title: "Member",
    name: "Mr. Kamazy",
    phone: "+94 78 324 3344",
    designation: "Designation",
    company: "Organization",
    profileImage: "",
    email: "",
  },
  {
    title: "Member",
    name: "MS Samsudeen",
    phone: "+94 71 554 8857",
    designation: "Software Engineer",
    company: "Graycorp Pty Ltd",
    profileImage: "/images/profiles/shiham-profile.png",
    email: "shiham247@gmail.com",
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
];
</script>
