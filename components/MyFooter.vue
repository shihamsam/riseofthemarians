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
          <img
            src="../public/images/logo.png"
            class="h-20"
            alt="St.Mary's College - Hambantota Logo"
          />
          <span
            class="hidden lg:block self-center lg:text-2xl font-semibold whitespace-nowrap dark:text-white"
            >St.Mary's College - Hambantota</span
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
              >Our Projects</NuxtLink
            >
          </li>
          <li>
            <NuxtLink to="/work" class="hover:underline me-4 md:me-6">
              Gallery</NuxtLink
            >
          </li>
          <li>
            <NuxtLink to="/committee" class="hover:underline me-4 md:me-6"
              >Committee</NuxtLink
            >
          </li>
          <li>
            <NuxtLink to="/donate" class="hover:underline me-4 md:me-6"
              >Donate</NuxtLink
            >
          </li>
        </ul>
      </div>
      <hr
        class="my-6 border-gray-200 sm:mx-auto dark:border-gray-700 lg:my-8"
      />

      <div class="mx-auto w-full max-w-screen-xl p-4 py-6 lg:py-8">
        <div class="sm:flex sm:items-center sm:justify-between">
          <span
            class="block text-sm text-gray-500 sm:text-center dark:text-gray-400"
            >© 2025
            <a href="/" class="hover:underline"
              >H/St.Mary's College PPA + School Development Committee + Rise Of
              The Marians </a
            >. All Rights Reserved.</span
          >
          <div class="flex mt-4 sm:justify-center sm:mt-0">
            <a
              href="https://web.facebook.com/profile.php?id=61554393763831"
              target="_blank"
              class="text-gray-500 hover:text-gray-900 dark:hover:text-white"
            >
              <svg
                class="w-6 h-6"
                aria-hidden="true"
                xmlns="http://www.w3.org/2000/svg"
                fill="currentColor"
                viewBox="0 0 24 24"
              >
                <path
                  fill-rule="evenodd"
                  d="M13.135 6H15V3h-1.865a4.147 4.147 0 0 0-4.142 4.142V9H7v3h2v9.938h3V12h2.021l.592-3H12V6.591A.6.6 0 0 1 12.592 6h.543Z"
                  clip-rule="evenodd"
                />
              </svg>

              <span class="sr-only">Facebook page</span>
            </a>
            <!-- 
            <a
              href="https://www.instagram.com/riseofthemarians/"
              target="_blank"
              class="text-gray-500 hover:text-gray-900 dark:hover:text-white ms-5"
            >
              <svg
                class="w-6 h-6"
                aria-hidden="true"
                xmlns="http://www.w3.org/2000/svg"
                fill="none"
                viewBox="0 0 24 24"
              >
                <path
                  fill="currentColor"
                  fill-rule="evenodd"
                  d="M3 8a5 5 0 0 1 5-5h8a5 5 0 0 1 5 5v8a5 5 0 0 1-5 5H8a5 5 0 0 1-5-5V8Zm5-3a3 3 0 0 0-3 3v8a3 3 0 0 0 3 3h8a3 3 0 0 0 3-3V8a3 3 0 0 0-3-3H8Zm7.597 2.214a1 1 0 0 1 1-1h.01a1 1 0 1 1 0 2h-.01a1 1 0 0 1-1-1ZM12 9a3 3 0 1 0 0 6 3 3 0 0 0 0-6Zm-5 3a5 5 0 1 1 10 0 5 5 0 0 1-10 0Z"
                  clip-rule="evenodd"
                />
              </svg>

              <span class="sr-only">Instagram Page</span>
            </a> -->
          </div>
        </div>
      </div>
    </div>
  </footer>
</template>
