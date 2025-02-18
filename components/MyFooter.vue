<template>
  <!-- <footer class="bg-white rounded-lg shadow-sm dark:bg-gray-900 m-4"> -->
  <footer
    class="px-4 py-1 bg-gray-100 dark:bg-gray-700 md:flex md:items-center md:justify-between"
  >
    <div class="w-full max-w-screen-xl mx-auto p-4 md:py-8">
      <div class="sm:flex sm:items-center sm:justify-between">
        <NuxtLink
          to="/"
          class="flex items-center space-x-3 rtl:space-x-reverse max-sm:mb-5"
        >
          <img src="../public/images/logo.jpg" class="h-12" alt="FBMV Logo" />
          <span
            class="self-center max-sm:hidden text-2xl font-semibold whitespace-nowrap dark:text-white"
            >P/FBMV Grade 6 - 2025</span
          >
          <span
            class="block sm:hidden self-center text-xl font-semibold whitespace-nowrap dark:text-white"
            >P/FBMV Grade 6 - 2025</span
          >
        </NuxtLink>
        <ul
          class="flex flex-wrap items-center mb-6 text-sm font-medium text-gray-500 sm:mb-0 dark:text-gray-400"
        >
          <li>
            <NuxtLink
              to="/"
              class="hover:underline me-4 md:me-6"
              aria-current="page"
              >Home</NuxtLink
            >
          </li>
          <li>
            <NuxtLink to="/project" class="hover:underline me-4 md:me-6"
              >Project</NuxtLink
            >
          </li>
          <li>
            <NuxtLink to="/work" class="hover:underline me-4 md:me-6"
              >Work Gallery</NuxtLink
            >
          </li>
          <li>
            <NuxtLink to="/committee" class="hover:underline me-4 md:me-6"
              >Committee</NuxtLink
            >
          </li>
        </ul>
      </div>
      <hr
        class="my-6 border-gray-200 sm:mx-auto dark:border-gray-700 lg:my-8"
      />
      <span
        class="block text-sm text-gray-500 sm:text-center dark:text-gray-400"
        >© 2025 <a href="/" class="hover:underline">P/FBMV Grade 6</a>. All
        Rights Reserved.</span
      >
    </div>
  </footer>
</template>
