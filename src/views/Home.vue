<template>
  <div class="h-screen flex flex-col antialiased">
    <header class="bg-lilac-dark">
      <div
        class="
        md:flex
        md:justify-between
        md:items-center
        md:w-full
        md:pl-6
        md:pr-4
        lg:pl-11
        flex-shrink-0
        2xl:max-w-7xl
        2xl:mx-auto">
        <div class="flex justify-between items-center px-3 sm:px-5 md:px-0 py-2.5 md:w-8/12 lg:w-9/12">
          <div>
            <svg
              class="h-7 w-7"
              viewBox="0 0 520 520"
              fill="none"
              xmlns="http://www.w3.org/2000/svg"
            >
              <path
                d="M187.432 271c-29.538 0-53.568 24.03-53.568 53.568v133.863c0 29.538 24.03 53.568 53.568 53.568C216.97 512 241 487.97 241 458.432V324.568C241 295.03 216.97 271 187.432 271z"
                fill="#cacaf0"
              />
              <path
                d="M103.863 271h-51.86c-28.596 0-51.86 23.265-51.86 51.86 0 28.596 23.265 51.86 51.86 51.86s51.86-23.265 51.86-51.86z"
                fill="#cacaf0"
              />
              <path
                d="M0 187.432C0 216.97 24.03 241 53.568 241h133.863C216.97 241 241 216.97 241 187.432s-24.03-53.568-53.568-53.568H53.568C24.03 133.863 0 157.894 0 187.432z"
                fill="#cacaf0"
              />
              <path
                d="M189.14 103.863H241v-51.86c0-28.596-23.265-51.86-51.86-51.86-28.596 0-51.86 23.265-51.86 51.86s23.264 51.86 51.86 51.86z"
                fill="#cacaf0"
              />
              <path
                d="M324.568 241c29.538 0 53.568-24.03 53.568-53.568V53.568C378.137 24.03 354.106 0 324.568 0S271 24.03 271 53.568v133.863C271 216.97 295.03 241 324.568 241z"
                fill="#cacaf0"
              />
              <path
                d="M408.137 241h51.86c28.596 0 51.86-23.265 51.86-51.86 0-28.596-23.265-51.86-51.86-51.86s-51.86 23.265-51.86 51.86z"
                fill="#cacaf0"
              />
              <g fill="#cacaf0">
                <path
                  d="M512 324.568C512 295.03 487.97 271 458.432 271H324.568C295.03 271 271 295.03 271 324.568s24.03 53.568 53.568 53.568h133.863c29.539.001 53.569-24.03 53.569-53.568z"
                />
                <path
                  d="M322.86 408.137H271v51.86c0 28.596 23.265 51.86 51.86 51.86 28.596 0 51.86-23.265 51.86-51.86s-23.264-51.86-51.86-51.86z"
                />
              </g>
            </svg>
          </div>
          <div class="flex-1 relative max-w-lg lg:max-w-xl ml-4 md:mr-4 lg:mr-5">
            <span class="absolute inset-y-0 left-0 flex items-center pl-2">
              <svg
                xmlns="http://www.w3.org/2000/svg"
                class="h-5 w-5 text-gray-50 opacity-70 focus:text-gray-900"
                viewBox="0 0 20 20"
                fill="currentColor"
              >
                <path
                  fill-rule="evenodd"
                  d="M8 4a4 4 0 100 8 4 4 0 000-8zM2 8a6 6 0 1110.89 3.476l4.817 4.817a1 1 0 01-1.414 1.414l-4.816-4.816A6 6 0 012 8z"
                  clip-rule="evenodd"
                />
              </svg>
            </span>
            <input
              type="text"
              class="
                block
                pl-9
                pr-4
                pt-2
                pb-2
                w-full
                bg-lilac-default
                rounded-md
                text-sm
                placeholder-gray-50 placeholder-opacity-70
                text-white
                focus:outline-none
                focus:text-white
              "
              placeholder="Search"
            />
          </div>
          <div class="ml-3 md:hidden">
            <button @click="toggleMenu" type="button" class="focus:outline-none">
              <svg
                xmlns="http://www.w3.org/2000/svg"
                class="mt-1 h-6 w-6 fill-current text-gray-50 opacity-70"
                fill="none"
                viewBox="0 0 24 24"
                stroke="currentColor"
              >
                <path
                  stroke-linecap="round"
                  stroke-linejoin="round"
                  stroke-width="2"
                  d="M4 6h16M4 12h8m-8 6h16"
                />
              </svg>
            </button>
          </div>
        </div>
        <nav
          class="md:flex md:justify-end md:items-center md:w-4/12 lg:w-3/12 md:relative"
          :class="{ hidden: !isOpen, block: isOpen }"
        >
          <div
            class="
              px-1
              pt-1
              pb-3
              border-b-2 border-lilac-black
              md:flex
              md:items-center
              md:border-0
              md:py-0
            "
          >
            <router-link
              to="#"
              class="
                px-2
                py-2
                block
                text-xs text-gray-50
                opacity-90
                bg-lilac-black
                rounded-md
                md:bg-lilac-dark
                md:opacity-75
                md:hover:bg-lilac-black
                md:hover:opacity-100
              "
              >Documentation</router-link
            >
            <router-link
              to="#"
              class="
                mt-1.5
                px-2
                py-1.5
                block
                text-xs text-gray-50
                opacity-75
                hover:opacity-100
                md:mt-0
                md:ml-1
                md:hover:bg-lilac-black
                md:rounded-md
              "
              >Support</router-link
            >
          </div>
          <div class="hidden md:flex md:items-end md:ml-2">
            <button
              @click="toggleDropdown"
              type="button"
              class="focus:outline-none"
            >
              <img
                class="h-7 w-7 rounded-full"
                src="../assets/profile.jpg"
                alt="profile"
              />
            </button>
          </div>
          <div :class="dropdown ? 'md:block' : 'md:hidden'">
            <button
              @click="dropdown = false"
              type="button"
              class="
                hidden
                md:block
                md:fixed
                md:opacity-0
                md:inset-0
                md:w-full
                md:h-full
                md:z-10
                md:cursor-default
              "
            ></button>
            <div
              class="
                px-1
                pt-1.5
                pb-2
                md:absolute
                md:right-0
                md:top-8
                md:bg-white
                md:w-44
                md:rounded-md
                md:shadow-lg
                md:z-10
                md:px-0
                md:pb-3
              "
            >
              <router-link
                to="#"
                class="
                  mt-1.5
                  px-2
                  py-1.5
                  block
                  text-xs text-gray-50
                  opacity-75
                  hover:opacity-100
                  md:text-gray-500
                  md:opacity-100
                  md:font-semibold
                  md:hover:bg-lilac-light
                  md:hover:text-white
                "
                >Profile</router-link
              >
              <router-link
                to="#"
                class="
                  mt-1.5
                  px-2
                  py-1.5
                  block
                  text-xs text-gray-50
                  opacity-75
                  hover:opacity-100
                  md:text-gray-500
                  md:opacity-100
                  md:font-semibold
                  md:hover:bg-lilac-light
                  md:hover:text-white
                "
                >Settings</router-link
              >
              <router-link
                to="#"
                class="
                  mt-1.5
                  px-2
                  py-1.5
                  block
                  text-xs text-gray-50
                  opacity-75
                  hover:opacity-100
                  md:text-gray-500
                  md:opacity-100
                  md:font-semibold
                  md:hover:bg-lilac-light
                  md:hover:text-white
                "
                >Logout</router-link
              >
            </div>
          </div>
        </nav>
      </div>
    </header>
    <div class="flex-1 md:flex md:justify-between md:w-full md:overflow-y-hidden 2xl:max-w-7xl 2xl:mx-auto">
      <main class="md:flex md:flex-col md:w-8/12 lg:w-9/12 md:flex-1 md:border-r border-gray-200">
        <div class="flex-1 lg:flex lg:flex-row lg:w-full md:flex md:flex-col md:overflow-y-hidden">
          <section class="px-3 sm:px-5 py-6 lg:w-4/12 lg:pl-11 ">
            <div class="sm:flex sm:justify-between sm:items-center lg:block">
              <div class="flex items-center">
                <div>
                  <img
                    class="h-10 w-10 rounded-full"
                    src="../assets/profile.jpg"
                    alt="picture"
                  />
                </div>
                <div class="ml-2.5">
                  <h2 class="text-sm font-medium text-gray-700">Benn Ajax</h2>
                  <div class="flex items-center -ml-0.5">
                    <svg
                      fill="currentColor"
                      viewBox="0 0 24 24"
                      class="h-5 w-5 fill-current text-gray-400"
                    >
                      <path
                        fill-rule="evenodd"
                        clip-rule="evenodd"
                        d="M12 2C6.477 2 2 6.463 2 11.97c0 4.404 2.865 8.14 6.839 9.458.5.092.682-.216.682-.48 0-.236-.008-.864-.013-1.695-2.782.602-3.369-1.337-3.369-1.337-.454-1.151-1.11-1.458-1.11-1.458-.908-.618.069-.606.069-.606 1.003.07 1.531 1.027 1.531 1.027.892 1.524 2.341 1.084 2.91.828.092-.643.35-1.083.636-1.332-2.22-.251-4.555-1.107-4.555-4.927 0-1.088.39-1.979 1.029-2.675-.103-.252-.446-1.266.098-2.638 0 0 .84-.268 2.75 1.022A9.606 9.606 0 0112 6.82c.85.004 1.705.114 2.504.336 1.909-1.29 2.747-1.022 2.747-1.022.546 1.372.202 2.386.1 2.638.64.696 1.028 1.587 1.028 2.675 0 3.83-2.339 4.673-4.566 4.92.359.307.678.915.678 1.846 0 1.332-.012 2.407-.012 2.734 0 .267.18.577.688.48C19.137 20.107 22 16.373 22 11.969 22 6.463 17.522 2 12 2z"
                      ></path>
                    </svg>
                    <span class="ml-1.5 text-gray-500 text-sm">bennajax</span>
                  </div>
                </div>
              </div>
              <div class="mt-8 sm:mt-0 lg:mt-8">
                <button
                  class="
                    py-2.5
                    w-full
                    bg-lilac-light
                    border border-lilac-black
                    rounded-md
                    focus:outline-none
                    sm:w-max
                    sm:px-3.5
                    sm:py-1.5
                    sm:hover:bg-white
                    sm:border-lilac-default
                    group
                    lg:block
                    lg:w-full
                  "
                  type="button"
                >
                  <span class="block text-gray-50 opacity-90 text-sm sm:group-hover:text-gray-700"
                    >New Project</span
                  >
                </button>
                <button
                  class="
                    mt-3.5
                    py-2.5
                    w-full
                    border border-gray-300
                    rounded-md
                    focus:outline-none
                    sm:mt-0
                    sm:ml-3
                    sm:w-max
                    sm:px-3.5
                    sm:py-1.5
                    sm:hover:bg-lilac-light
                    group
                    lg:mt-3.5
                    lg:ml-0
                    lg:block
                    lg:w-full
                  "
                  type="button"
                >
                  <span class="block text-gray-700 text-sm sm:group-hover:text-gray-50 sm:group-hover:opacity-90 ">Invite Team</span>
                </button>
              </div>
            </div>
            <div class="mt-6 sm:flex sm:items-center lg:block">
              <div class="flex items-center">
                <svg
                  xmlns="http://www.w3.org/2000/svg"
                  class="h-4 w-4 fill-current text-gray-400"
                  viewBox="0 0 20 20"
                  fill="currentColor"
                >
                  <path
                    fill-rule="evenodd"
                    d="M6.267 3.455a3.066 3.066 0 001.745-.723 3.066 3.066 0 013.976 0 3.066 3.066 0 001.745.723 3.066 3.066 0 012.812 2.812c.051.643.304 1.254.723 1.745a3.066 3.066 0 010 3.976 3.066 3.066 0 00-.723 1.745 3.066 3.066 0 01-2.812 2.812 3.066 3.066 0 00-1.745.723 3.066 3.066 0 01-3.976 0 3.066 3.066 0 00-1.745-.723 3.066 3.066 0 01-2.812-2.812 3.066 3.066 0 00-.723-1.745 3.066 3.066 0 010-3.976 3.066 3.066 0 00.723-1.745 3.066 3.066 0 012.812-2.812zm7.44 5.252a1 1 0 00-1.414-1.414L9 10.586 7.707 9.293a1 1 0 00-1.414 1.414l2 2a1 1 0 001.414 0l4-4z"
                    clip-rule="evenodd"
                  />
                </svg>
                <span class="ml-1.5 text-gray-500 text-xs font-medium"
                  >Pro Member</span
                >
              </div>
              <div class="mt-6 sm:mt-0 sm:ml-6 flex items-center lg:mt-4 lg:ml-0">
                <svg
                  xmlns="http://www.w3.org/2000/svg"
                  class="h-4 w-4 fill-current text-gray-400"
                  viewBox="0 0 20 20"
                  fill="currentColor"
                >
                  <path
                    d="M7 3a1 1 0 000 2h6a1 1 0 100-2H7zM4 7a1 1 0 011-1h10a1 1 0 110 2H5a1 1 0 01-1-1zM2 11a2 2 0 012-2h12a2 2 0 012 2v4a2 2 0 01-2 2H4a2 2 0 01-2-2v-4z"
                  />
                </svg>
                <span class="ml-1.5 text-gray-500 text-xs font-medium"
                  >8 Projects</span
                >
              </div>
            </div>
          </section>
          <section class="md:flex md:flex-col md:overflow-y-hidden lg:w-8/12 lg:border-l border-gray-200 ">
            <div
              class="
                py-4
                flex
                justify-between
                items-center
                border-t border-b
                text-gray-300
              "
            >
              <h2 class="mx-3 sm:mx-5 text-lg font-bold text-gray-800 lg:text-gray-600">Projects</h2>
              <button
                class="
                  flex
                  items-center
                  px-2
                  py-1
                  mx-3 sm:mx-5
                  border border-gray-300
                  rounded-md
                  focus:outline-none
                "
              >
                <svg
                  xmlns="http://www.w3.org/2000/svg"
                  fill="none"
                  viewBox="0 0 24 24"
                  stroke="currentColor"
                  class="h-4 w-4 text-gray-500"
                >
                  <path
                    stroke-linecap="round"
                    stroke-linejoin="round"
                    stroke-width="2"
                    d="M3 4h13M3 8h9m-9 4h6m4 0l4-4m0 0l4 4m-4-4v12"
                  ></path>
                </svg>
                <span class="ml-1.5 text-xs font-bold text-gray-700">Sort</span>
                <svg
                  xmlns="http://www.w3.org/2000/svg"
                  class="h-5 w-5 ml-1.5 text-gray-400"
                  viewBox="0 0 20 20"
                  fill="currentColor"
                >
                  <path
                    fill-rule="evenodd"
                    d="M5.293 7.293a1 1 0 011.414 0L10 10.586l3.293-3.293a1 1 0 111.414 1.414l-4 4a1 1 0 01-1.414 0l-4-4a1 1 0 010-1.414z"
                    clip-rule="evenodd"
                  />
                </svg>
              </button>
            </div>
            <section class="md:flex md:flex-col md:overflow-y-hidden">
              <div class="divide-y divide-gray-300 md:overflow-y-auto scrollbar scrollbar-thin scrollbar-thumb-gray-400 scrollbar-thumb-rounded-md scrollbar-track-gray-200">
                <router-link
                  to="#"
                  class="px-3 sm:px-5 flex justify-between items-center py-3"
                >
                  <div>
                    <p>
                      <span
                        aria-hidden="true"
                        class="
                          mt-px
                          inline-block
                          h-2.5
                          w-2.5
                          rounded-full
                          bg-green-500
                        "
                      ></span>
                      <span class="ml-3 text-sm font-semibold text-gray-700"
                        >Workcation</span
                      >
                    </p>
                    <div class="flex items-center -ml-1 mt-1.5">
                      <svg
                        fill="currentColor"
                        viewBox="0 0 24 24"
                        class="h-5 w-5 fill-current text-gray-400"
                      >
                        <path
                          fill-rule="evenodd"
                          clip-rule="evenodd"
                          d="M12 2C6.477 2 2 6.463 2 11.97c0 4.404 2.865 8.14 6.839 9.458.5.092.682-.216.682-.48 0-.236-.008-.864-.013-1.695-2.782.602-3.369-1.337-3.369-1.337-.454-1.151-1.11-1.458-1.11-1.458-.908-.618.069-.606.069-.606 1.003.07 1.531 1.027 1.531 1.027.892 1.524 2.341 1.084 2.91.828.092-.643.35-1.083.636-1.332-2.22-.251-4.555-1.107-4.555-4.927 0-1.088.39-1.979 1.029-2.675-.103-.252-.446-1.266.098-2.638 0 0 .84-.268 2.75 1.022A9.606 9.606 0 0112 6.82c.85.004 1.705.114 2.504.336 1.909-1.29 2.747-1.022 2.747-1.022.546 1.372.202 2.386.1 2.638.64.696 1.028 1.587 1.028 2.675 0 3.83-2.339 4.673-4.566 4.92.359.307.678.915.678 1.846 0 1.332-.012 2.407-.012 2.734 0 .267.18.577.688.48C19.137 20.107 22 16.373 22 11.969 22 6.463 17.522 2 12 2z"
                        ></path>
                      </svg>
                      <span class="ml-1.5 text-gray-500 text-sm"
                        >bennajax/workcation</span
                      >
                    </div>
                  </div>
                  <svg
                    xmlns="http://www.w3.org/2000/svg"
                    class="sm:hidden h-5 w-5 fill-current text-gray-400"
                    viewBox="0 0 20 20"
                    fill="currentColor"
                  >
                    <path
                      fill-rule="evenodd"
                      d="M7.293 14.707a1 1 0 010-1.414L10.586 10 7.293 6.707a1 1 0 011.414-1.414l4 4a1 1 0 010 1.414l-4 4a1 1 0 01-1.414 0z"
                      clip-rule="evenodd"
                    />
                  </svg>
                  <div class="hidden sm:block">
                    <div class="mt-px flex justify-end items-center">
                      <span class="text-xs text-gray-400 font-medium">Visit Site</span>
                      <svg xmlns="http://www.w3.org/2000/svg" class="ml-3 h-4 w-4 text-yellow-400" viewBox="0 0 20 20" fill="currentColor">
                        <path d="M9.049 2.927c.3-.921 1.603-.921 1.902 0l1.07 3.292a1 1 0 00.95.69h3.462c.969 0 1.371 1.24.588 1.81l-2.8 2.034a1 1 0 00-.364 1.118l1.07 3.292c.3.921-.755 1.688-1.54 1.118l-2.8-2.034a1 1 0 00-1.175 0l-2.8 2.034c-.784.57-1.838-.197-1.539-1.118l1.07-3.292a1 1 0 00-.364-1.118L2.98 8.72c-.783-.57-.38-1.81.588-1.81h3.461a1 1 0 00.951-.69l1.07-3.292z" />
                      </svg>
                    </div>
                    <p class="mt-3 text-xs text-gray-400">NextJS . Last deploy 6h ago . United States</p>
                  </div>
                </router-link>
                <router-link
                  to="#"
                  class="px-3 sm:px-5 flex justify-between items-center py-3"
                >
                  <div>
                    <p>
                      <span
                        aria-hidden="true"
                        class="
                          mt-px
                          inline-block
                          h-2.5
                          w-2.5
                          rounded-full
                          bg-green-500
                        "
                      ></span>
                      <span class="ml-3 text-sm font-semibold text-gray-700"
                      >Easywire</span
                      >
                    </p>
                    <div class="flex items-center -ml-1 mt-1.5">
                      <svg
                        fill="currentColor"
                        viewBox="0 0 24 24"
                        class="h-5 w-5 fill-current text-gray-400"
                      >
                        <path
                          fill-rule="evenodd"
                          clip-rule="evenodd"
                          d="M12 2C6.477 2 2 6.463 2 11.97c0 4.404 2.865 8.14 6.839 9.458.5.092.682-.216.682-.48 0-.236-.008-.864-.013-1.695-2.782.602-3.369-1.337-3.369-1.337-.454-1.151-1.11-1.458-1.11-1.458-.908-.618.069-.606.069-.606 1.003.07 1.531 1.027 1.531 1.027.892 1.524 2.341 1.084 2.91.828.092-.643.35-1.083.636-1.332-2.22-.251-4.555-1.107-4.555-4.927 0-1.088.39-1.979 1.029-2.675-.103-.252-.446-1.266.098-2.638 0 0 .84-.268 2.75 1.022A9.606 9.606 0 0112 6.82c.85.004 1.705.114 2.504.336 1.909-1.29 2.747-1.022 2.747-1.022.546 1.372.202 2.386.1 2.638.64.696 1.028 1.587 1.028 2.675 0 3.83-2.339 4.673-4.566 4.92.359.307.678.915.678 1.846 0 1.332-.012 2.407-.012 2.734 0 .267.18.577.688.48C19.137 20.107 22 16.373 22 11.969 22 6.463 17.522 2 12 2z"
                        ></path>
                      </svg>
                      <span class="ml-1.5 text-gray-500 text-sm"
                      >bennajax/easywire</span
                      >
                    </div>
                  </div>
                  <svg
                    xmlns="http://www.w3.org/2000/svg"
                    class="sm:hidden h-5 w-5 fill-current text-gray-400"
                    viewBox="0 0 20 20"
                    fill="currentColor"
                  >
                    <path
                      fill-rule="evenodd"
                      d="M7.293 14.707a1 1 0 010-1.414L10.586 10 7.293 6.707a1 1 0 011.414-1.414l4 4a1 1 0 010 1.414l-4 4a1 1 0 01-1.414 0z"
                      clip-rule="evenodd"
                    />
                  </svg>
                  <div class="hidden sm:block">
                    <div class="mt-px flex justify-end items-center">
                      <span class="text-xs text-gray-400 font-medium">Visit Site</span>
                      <svg xmlns="http://www.w3.org/2000/svg" class="ml-3 h-4 w-4 text-yellow-400" viewBox="0 0 20 20" fill="currentColor">
                        <path d="M9.049 2.927c.3-.921 1.603-.921 1.902 0l1.07 3.292a1 1 0 00.95.69h3.462c.969 0 1.371 1.24.588 1.81l-2.8 2.034a1 1 0 00-.364 1.118l1.07 3.292c.3.921-.755 1.688-1.54 1.118l-2.8-2.034a1 1 0 00-1.175 0l-2.8 2.034c-.784.57-1.838-.197-1.539-1.118l1.07-3.292a1 1 0 00-.364-1.118L2.98 8.72c-.783-.57-.38-1.81.588-1.81h3.461a1 1 0 00.951-.69l1.07-3.292z" />
                      </svg>
                    </div>
                    <p class="mt-3 text-xs text-gray-400">VueJS . Last deploy 7h ago . United States</p>
                  </div>
                </router-link>
                <router-link
                  to="#"
                  class="px-3 sm:px-5 flex justify-between items-center py-3"
                >
                  <div>
                    <p>
                      <span
                        aria-hidden="true"
                        class="
                          mt-px
                          inline-block
                          h-2.5
                          w-2.5
                          rounded-full
                          bg-gray-400
                        "
                      ></span>
                      <span class="ml-3 text-sm font-semibold text-gray-700"
                      >Workflow</span
                      >
                    </p>
                    <div class="flex items-center -ml-1 mt-1.5">
                      <svg
                        fill="currentColor"
                        viewBox="0 0 24 24"
                        class="h-5 w-5 fill-current text-gray-400"
                      >
                        <path
                          fill-rule="evenodd"
                          clip-rule="evenodd"
                          d="M12 2C6.477 2 2 6.463 2 11.97c0 4.404 2.865 8.14 6.839 9.458.5.092.682-.216.682-.48 0-.236-.008-.864-.013-1.695-2.782.602-3.369-1.337-3.369-1.337-.454-1.151-1.11-1.458-1.11-1.458-.908-.618.069-.606.069-.606 1.003.07 1.531 1.027 1.531 1.027.892 1.524 2.341 1.084 2.91.828.092-.643.35-1.083.636-1.332-2.22-.251-4.555-1.107-4.555-4.927 0-1.088.39-1.979 1.029-2.675-.103-.252-.446-1.266.098-2.638 0 0 .84-.268 2.75 1.022A9.606 9.606 0 0112 6.82c.85.004 1.705.114 2.504.336 1.909-1.29 2.747-1.022 2.747-1.022.546 1.372.202 2.386.1 2.638.64.696 1.028 1.587 1.028 2.675 0 3.83-2.339 4.673-4.566 4.92.359.307.678.915.678 1.846 0 1.332-.012 2.407-.012 2.734 0 .267.18.577.688.48C19.137 20.107 22 16.373 22 11.969 22 6.463 17.522 2 12 2z"
                        ></path>
                      </svg>
                      <span class="ml-1.5 text-gray-500 text-sm"
                      >bennajax/workflow</span
                      >
                    </div>
                  </div>
                  <svg
                    xmlns="http://www.w3.org/2000/svg"
                    class="sm:hidden h-5 w-5 fill-current text-gray-400"
                    viewBox="0 0 20 20"
                    fill="currentColor"
                  >
                    <path
                      fill-rule="evenodd"
                      d="M7.293 14.707a1 1 0 010-1.414L10.586 10 7.293 6.707a1 1 0 011.414-1.414l4 4a1 1 0 010 1.414l-4 4a1 1 0 01-1.414 0z"
                      clip-rule="evenodd"
                    />
                  </svg>
                  <div class="hidden sm:block">
                    <div class="mt-px flex justify-end items-center">
                      <span class="text-xs text-gray-400 font-medium">Visit Site</span>
                      <svg xmlns="http://www.w3.org/2000/svg" class="ml-3 h-4 w-4 text-gray-300" viewBox="0 0 20 20" fill="currentColor">
                        <path d="M9.049 2.927c.3-.921 1.603-.921 1.902 0l1.07 3.292a1 1 0 00.95.69h3.462c.969 0 1.371 1.24.588 1.81l-2.8 2.034a1 1 0 00-.364 1.118l1.07 3.292c.3.921-.755 1.688-1.54 1.118l-2.8-2.034a1 1 0 00-1.175 0l-2.8 2.034c-.784.57-1.838-.197-1.539-1.118l1.07-3.292a1 1 0 00-.364-1.118L2.98 8.72c-.783-.57-.38-1.81.588-1.81h3.461a1 1 0 00.951-.69l1.07-3.292z" />
                      </svg>
                    </div>
                    <p class="mt-3 text-xs text-gray-400">NextJS . Last deploy 6h ago . United States</p>
                  </div>
                </router-link>
                <router-link
                  to="#"
                  class="px-3 sm:px-5 flex justify-between items-center py-3"
                >
                  <div>
                    <p>
                      <span
                        aria-hidden="true"
                        class="
                          mt-px
                          inline-block
                          h-2.5
                          w-2.5
                          rounded-full
                          bg-green-500
                        "
                      ></span>
                      <span class="ml-3 text-sm font-semibold text-gray-700"
                      >Maxsio</span
                      >
                    </p>
                    <div class="flex items-center -ml-1 mt-1.5">
                      <svg
                        fill="currentColor"
                        viewBox="0 0 24 24"
                        class="h-5 w-5 fill-current text-gray-400"
                      >
                        <path
                          fill-rule="evenodd"
                          clip-rule="evenodd"
                          d="M12 2C6.477 2 2 6.463 2 11.97c0 4.404 2.865 8.14 6.839 9.458.5.092.682-.216.682-.48 0-.236-.008-.864-.013-1.695-2.782.602-3.369-1.337-3.369-1.337-.454-1.151-1.11-1.458-1.11-1.458-.908-.618.069-.606.069-.606 1.003.07 1.531 1.027 1.531 1.027.892 1.524 2.341 1.084 2.91.828.092-.643.35-1.083.636-1.332-2.22-.251-4.555-1.107-4.555-4.927 0-1.088.39-1.979 1.029-2.675-.103-.252-.446-1.266.098-2.638 0 0 .84-.268 2.75 1.022A9.606 9.606 0 0112 6.82c.85.004 1.705.114 2.504.336 1.909-1.29 2.747-1.022 2.747-1.022.546 1.372.202 2.386.1 2.638.64.696 1.028 1.587 1.028 2.675 0 3.83-2.339 4.673-4.566 4.92.359.307.678.915.678 1.846 0 1.332-.012 2.407-.012 2.734 0 .267.18.577.688.48C19.137 20.107 22 16.373 22 11.969 22 6.463 17.522 2 12 2z"
                        ></path>
                      </svg>
                      <span class="ml-1.5 text-gray-500 text-sm"
                      >bennajax/maxsio</span
                      >
                    </div>
                  </div>
                  <svg
                    xmlns="http://www.w3.org/2000/svg"
                    class="sm:hidden h-5 w-5 fill-current text-gray-400"
                    viewBox="0 0 20 20"
                    fill="currentColor"
                  >
                    <path
                      fill-rule="evenodd"
                      d="M7.293 14.707a1 1 0 010-1.414L10.586 10 7.293 6.707a1 1 0 011.414-1.414l4 4a1 1 0 010 1.414l-4 4a1 1 0 01-1.414 0z"
                      clip-rule="evenodd"
                    />
                  </svg>
                  <div class="hidden sm:block">
                    <div class="mt-px flex justify-end items-center">
                      <span class="text-xs text-gray-400 font-medium">Visit Site</span>
                      <svg xmlns="http://www.w3.org/2000/svg" class="ml-3 h-4 w-4 text-yellow-400" viewBox="0 0 20 20" fill="currentColor">
                        <path d="M9.049 2.927c.3-.921 1.603-.921 1.902 0l1.07 3.292a1 1 0 00.95.69h3.462c.969 0 1.371 1.24.588 1.81l-2.8 2.034a1 1 0 00-.364 1.118l1.07 3.292c.3.921-.755 1.688-1.54 1.118l-2.8-2.034a1 1 0 00-1.175 0l-2.8 2.034c-.784.57-1.838-.197-1.539-1.118l1.07-3.292a1 1 0 00-.364-1.118L2.98 8.72c-.783-.57-.38-1.81.588-1.81h3.461a1 1 0 00.951-.69l1.07-3.292z" />
                      </svg>
                    </div>
                    <p class="mt-3 text-xs text-gray-400">VueJS . Last deploy 6h ago . United States</p>
                  </div>
                </router-link>
                <router-link
                  to="#"
                  class="px-3 sm:px-5 flex justify-between items-center py-3"
                >
                  <div>
                    <p>
                      <span
                        aria-hidden="true"
                        class="
                          mt-px
                          inline-block
                          h-2.5
                          w-2.5
                          rounded-full
                          bg-gray-400
                        "
                      ></span>
                      <span class="ml-3 text-sm font-semibold text-gray-700"
                      >Personal Website</span
                      >
                    </p>
                    <div class="flex items-center -ml-1 mt-1.5">
                      <svg
                        fill="currentColor"
                        viewBox="0 0 24 24"
                        class="h-5 w-5 fill-current text-gray-400"
                      >
                        <path
                          fill-rule="evenodd"
                          clip-rule="evenodd"
                          d="M12 2C6.477 2 2 6.463 2 11.97c0 4.404 2.865 8.14 6.839 9.458.5.092.682-.216.682-.48 0-.236-.008-.864-.013-1.695-2.782.602-3.369-1.337-3.369-1.337-.454-1.151-1.11-1.458-1.11-1.458-.908-.618.069-.606.069-.606 1.003.07 1.531 1.027 1.531 1.027.892 1.524 2.341 1.084 2.91.828.092-.643.35-1.083.636-1.332-2.22-.251-4.555-1.107-4.555-4.927 0-1.088.39-1.979 1.029-2.675-.103-.252-.446-1.266.098-2.638 0 0 .84-.268 2.75 1.022A9.606 9.606 0 0112 6.82c.85.004 1.705.114 2.504.336 1.909-1.29 2.747-1.022 2.747-1.022.546 1.372.202 2.386.1 2.638.64.696 1.028 1.587 1.028 2.675 0 3.83-2.339 4.673-4.566 4.92.359.307.678.915.678 1.846 0 1.332-.012 2.407-.012 2.734 0 .267.18.577.688.48C19.137 20.107 22 16.373 22 11.969 22 6.463 17.522 2 12 2z"
                        ></path>
                      </svg>
                      <span class="ml-1.5 text-gray-500 text-sm"
                      >bennajax/personal-website</span
                      >
                    </div>
                  </div>
                  <svg
                    xmlns="http://www.w3.org/2000/svg"
                    class="sm:hidden h-5 w-5 fill-current text-gray-400"
                    viewBox="0 0 20 20"
                    fill="currentColor"
                  >
                    <path
                      fill-rule="evenodd"
                      d="M7.293 14.707a1 1 0 010-1.414L10.586 10 7.293 6.707a1 1 0 011.414-1.414l4 4a1 1 0 010 1.414l-4 4a1 1 0 01-1.414 0z"
                      clip-rule="evenodd"
                    />
                  </svg>
                  <div class="hidden sm:block">
                    <div class="mt-px flex justify-end items-center">
                      <span class="text-xs text-gray-400 font-medium">Visit Site</span>
                      <svg xmlns="http://www.w3.org/2000/svg" class="ml-3 h-4 w-4 text-gray-300" viewBox="0 0 20 20" fill="currentColor">
                        <path d="M9.049 2.927c.3-.921 1.603-.921 1.902 0l1.07 3.292a1 1 0 00.95.69h3.462c.969 0 1.371 1.24.588 1.81l-2.8 2.034a1 1 0 00-.364 1.118l1.07 3.292c.3.921-.755 1.688-1.54 1.118l-2.8-2.034a1 1 0 00-1.175 0l-2.8 2.034c-.784.57-1.838-.197-1.539-1.118l1.07-3.292a1 1 0 00-.364-1.118L2.98 8.72c-.783-.57-.38-1.81.588-1.81h3.461a1 1 0 00.951-.69l1.07-3.292z" />
                      </svg>
                    </div>
                    <p class="mt-3 text-xs text-gray-400">NextJS . Last deploy 6h ago . United States</p>
                  </div>
                </router-link>
                <router-link
                  to="#"
                  class="px-3 sm:px-5 flex justify-between items-center py-3"
                >
                  <div>
                    <p>
                      <span
                        aria-hidden="true"
                        class="
                          mt-px
                          inline-block
                          h-2.5
                          w-2.5
                          rounded-full
                          bg-gray-400
                        "
                      ></span>
                      <span class="ml-3 text-sm font-semibold text-gray-700"
                      >Talk Slides</span
                      >
                    </p>
                    <div class="flex items-center -ml-1 mt-1.5">
                      <svg
                        fill="currentColor"
                        viewBox="0 0 24 24"
                        class="h-5 w-5 fill-current text-gray-400"
                      >
                        <path
                          fill-rule="evenodd"
                          clip-rule="evenodd"
                          d="M12 2C6.477 2 2 6.463 2 11.97c0 4.404 2.865 8.14 6.839 9.458.5.092.682-.216.682-.48 0-.236-.008-.864-.013-1.695-2.782.602-3.369-1.337-3.369-1.337-.454-1.151-1.11-1.458-1.11-1.458-.908-.618.069-.606.069-.606 1.003.07 1.531 1.027 1.531 1.027.892 1.524 2.341 1.084 2.91.828.092-.643.35-1.083.636-1.332-2.22-.251-4.555-1.107-4.555-4.927 0-1.088.39-1.979 1.029-2.675-.103-.252-.446-1.266.098-2.638 0 0 .84-.268 2.75 1.022A9.606 9.606 0 0112 6.82c.85.004 1.705.114 2.504.336 1.909-1.29 2.747-1.022 2.747-1.022.546 1.372.202 2.386.1 2.638.64.696 1.028 1.587 1.028 2.675 0 3.83-2.339 4.673-4.566 4.92.359.307.678.915.678 1.846 0 1.332-.012 2.407-.012 2.734 0 .267.18.577.688.48C19.137 20.107 22 16.373 22 11.969 22 6.463 17.522 2 12 2z"
                        ></path>
                      </svg>
                      <span class="ml-1.5 text-gray-500 text-sm"
                      >bennajax/talk-slides</span
                      >
                    </div>
                  </div>
                  <svg
                    xmlns="http://www.w3.org/2000/svg"
                    class="sm:hidden h-5 w-5 fill-current text-gray-400"
                    viewBox="0 0 20 20"
                    fill="currentColor"
                  >
                    <path
                      fill-rule="evenodd"
                      d="M7.293 14.707a1 1 0 010-1.414L10.586 10 7.293 6.707a1 1 0 011.414-1.414l4 4a1 1 0 010 1.414l-4 4a1 1 0 01-1.414 0z"
                      clip-rule="evenodd"
                    />
                  </svg>
                  <div class="hidden sm:block">
                    <div class="mt-px flex justify-end items-center">
                      <span class="text-xs text-gray-400 font-medium">Visit Site</span>
                      <svg xmlns="http://www.w3.org/2000/svg" class="ml-3 h-4 w-4 text-gray-300" viewBox="0 0 20 20" fill="currentColor">
                        <path d="M9.049 2.927c.3-.921 1.603-.921 1.902 0l1.07 3.292a1 1 0 00.95.69h3.462c.969 0 1.371 1.24.588 1.81l-2.8 2.034a1 1 0 00-.364 1.118l1.07 3.292c.3.921-.755 1.688-1.54 1.118l-2.8-2.034a1 1 0 00-1.175 0l-2.8 2.034c-.784.57-1.838-.197-1.539-1.118l1.07-3.292a1 1 0 00-.364-1.118L2.98 8.72c-.783-.57-.38-1.81.588-1.81h3.461a1 1 0 00.951-.69l1.07-3.292z" />
                      </svg>
                    </div>
                    <p class="mt-3 text-xs text-gray-400">NextJS . Last deploy 6h ago . United States</p>
                  </div>
                </router-link>
                <router-link
                  to="#"
                  class="px-3 sm:px-5 flex justify-between items-center py-3"
                >
                  <div>
                    <p>
                      <span
                        aria-hidden="true"
                        class="
                          mt-px
                          inline-block
                          h-2.5
                          w-2.5
                          rounded-full
                          bg-green-500
                        "
                      ></span>
                      <span class="ml-3 text-sm font-semibold text-gray-700"
                      >Digest</span
                      >
                    </p>
                    <div class="flex items-center -ml-1 mt-1.5">
                      <svg
                        fill="currentColor"
                        viewBox="0 0 24 24"
                        class="h-5 w-5 fill-current text-gray-400"
                      >
                        <path
                          fill-rule="evenodd"
                          clip-rule="evenodd"
                          d="M12 2C6.477 2 2 6.463 2 11.97c0 4.404 2.865 8.14 6.839 9.458.5.092.682-.216.682-.48 0-.236-.008-.864-.013-1.695-2.782.602-3.369-1.337-3.369-1.337-.454-1.151-1.11-1.458-1.11-1.458-.908-.618.069-.606.069-.606 1.003.07 1.531 1.027 1.531 1.027.892 1.524 2.341 1.084 2.91.828.092-.643.35-1.083.636-1.332-2.22-.251-4.555-1.107-4.555-4.927 0-1.088.39-1.979 1.029-2.675-.103-.252-.446-1.266.098-2.638 0 0 .84-.268 2.75 1.022A9.606 9.606 0 0112 6.82c.85.004 1.705.114 2.504.336 1.909-1.29 2.747-1.022 2.747-1.022.546 1.372.202 2.386.1 2.638.64.696 1.028 1.587 1.028 2.675 0 3.83-2.339 4.673-4.566 4.92.359.307.678.915.678 1.846 0 1.332-.012 2.407-.012 2.734 0 .267.18.577.688.48C19.137 20.107 22 16.373 22 11.969 22 6.463 17.522 2 12 2z"
                        ></path>
                      </svg>
                      <span class="ml-1.5 text-gray-500 text-sm"
                      >bennajax/digest</span
                      >
                    </div>
                  </div>
                  <svg
                    xmlns="http://www.w3.org/2000/svg"
                    class="sm:hidden h-5 w-5 fill-current text-gray-400"
                    viewBox="0 0 20 20"
                    fill="currentColor"
                  >
                    <path
                      fill-rule="evenodd"
                      d="M7.293 14.707a1 1 0 010-1.414L10.586 10 7.293 6.707a1 1 0 011.414-1.414l4 4a1 1 0 010 1.414l-4 4a1 1 0 01-1.414 0z"
                      clip-rule="evenodd"
                    />
                  </svg>
                  <div class="hidden sm:block">
                    <div class="mt-px flex justify-end items-center">
                      <span class="text-xs text-gray-400 font-medium">Visit Site</span>
                      <svg xmlns="http://www.w3.org/2000/svg" class="ml-3 h-4 w-4 text-yellow-400" viewBox="0 0 20 20" fill="currentColor">
                        <path d="M9.049 2.927c.3-.921 1.603-.921 1.902 0l1.07 3.292a1 1 0 00.95.69h3.462c.969 0 1.371 1.24.588 1.81l-2.8 2.034a1 1 0 00-.364 1.118l1.07 3.292c.3.921-.755 1.688-1.54 1.118l-2.8-2.034a1 1 0 00-1.175 0l-2.8 2.034c-.784.57-1.838-.197-1.539-1.118l1.07-3.292a1 1 0 00-.364-1.118L2.98 8.72c-.783-.57-.38-1.81.588-1.81h3.461a1 1 0 00.951-.69l1.07-3.292z" />
                      </svg>
                    </div>
                    <p class="mt-3 text-xs text-gray-400">VueJS . Last deploy 6h ago . United States</p>
                  </div>
                </router-link>
              </div>
            </section>
          </section>
        </div>
      </main>
      <aside class="px-4 py-6 md:pb-1.5 bg-gray-100 md:w-4/12 lg:w-3/12 md:pl-4 md:pr-2 md:flex md:flex-col md:overflow-y-hidden">
        <h2 class="text-xs font-bold text-gray-800">Activity</h2>
        <section class="mt-3 md:flex md:overflow-y-hidden">
          <div class="divide-y divide-gray-300 md:overflow-y-auto scrollbar scrollbar-thin scrollbar-thumb-gray-400 scrollbar-thumb-rounded-md scrollbar-track-gray-200">
            <div class="py-3.5 md:pr-1 flex justify-between items-start">
              <img class="flex-shrink-0 h-6 w-6 rounded-full" src="../assets/profile.jpg" alt="picture">
              <div class="flex-1 ml-3">
                <h3 class="text-xs font-bold text-gray-900">You</h3>
                <p class="mt-1.5 text-xs text-gray-500">Deployed Workcation (2d89f0c8 in master) to production</p>
              </div>
              <time class="flex-shrink-0 ml-3 text-xs text-gray-500 ">1h</time>
            </div>
            <div class="py-3.5 md:pr-1 flex justify-between items-start">
              <img class="flex-shrink-0 h-6 w-6 rounded-full" src="../assets/profile.jpg" alt="picture">
              <div class="flex-1 ml-3">
                <h3 class="text-xs font-bold text-gray-900">You</h3>
                <p class="mt-1.5 text-xs text-gray-500">Deployed EasyWire (2d89f0c8 in master) to production</p>
              </div>
              <time class="flex-shrink-0 ml-3 text-xs text-gray-500 ">1d</time>
            </div>
            <div class="py-3.5 md:pr-1 flex justify-between items-start">
              <img class="flex-shrink-0 h-6 w-6 rounded-full" src="../assets/profile.jpg" alt="picture">
              <div class="flex-1 ml-3">
                <h3 class="text-xs font-bold text-gray-900">You</h3>
                <p class="mt-1.5 text-xs text-gray-500">Deployed Workflow (2d89f0c8 in master) to production</p>
              </div>
              <time class="flex-shrink-0 ml-3 text-xs text-gray-500 ">12h</time>
            </div>
            <div class="py-3.5 md:pr-1 flex justify-between items-start">
              <img class="flex-shrink-0 h-6 w-6 rounded-full" src="../assets/profile.jpg" alt="picture">
              <div class="flex-1 ml-3">
                <h3 class="text-xs font-bold text-gray-900">You</h3>
                <p class="mt-1.5 text-xs text-gray-500">Deployed Maxsio (2d89f0c8 in master) to production</p>
              </div>
              <time class="flex-shrink-0 ml-3 text-xs text-gray-500 ">5d</time>
            </div>
            <div class="py-3.5 md:pr-1 flex justify-between items-start">
              <img class="flex-shrink-0 h-6 w-6 rounded-full" src="../assets/profile.jpg" alt="picture">
              <div class="flex-1 ml-3">
                <h3 class="text-xs font-bold text-gray-900">You</h3>
                <p class="mt-1.5 text-xs text-gray-500">Deployed Workcation (2d89f0c8 in master) to production</p>
              </div>
              <time class="flex-shrink-0 ml-3 text-xs text-gray-500 ">1h</time>
            </div>
            <div class="py-3.5 md:pr-1 flex justify-between items-start">
              <img class="flex-shrink-0 h-6 w-6 rounded-full" src="../assets/profile.jpg" alt="picture">
              <div class="flex-1 ml-3">
                <h3 class="text-xs font-bold text-gray-900">You</h3>
                <p class="mt-1.5 text-xs text-gray-500">Deployed EasyWire (2d89f0c8 in master) to production</p>
              </div>
              <time class="flex-shrink-0 ml-3 text-xs text-gray-500 ">1d</time>
            </div>
            <div class="py-3.5 md:pr-1 flex justify-between items-start">
              <img class="flex-shrink-0 h-6 w-6 rounded-full" src="../assets/profile.jpg" alt="picture">
              <div class="flex-1 ml-3">
                <h3 class="text-xs font-bold text-gray-900">You</h3>
                <p class="mt-1.5 text-xs text-gray-500">Deployed Workflow (2d89f0c8 in master) to production</p>
              </div>
              <time class="flex-shrink-0 ml-3 text-xs text-gray-500 ">12h</time>
            </div>
            <div class="py-3.5 md:pr-1 flex justify-between items-start">
              <img class="flex-shrink-0 h-6 w-6 rounded-full" src="../assets/profile.jpg" alt="picture">
              <div class="flex-1 ml-3">
                <h3 class="text-xs font-bold text-gray-900">You</h3>
                <p class="mt-1.5 text-xs text-gray-500">Deployed Maxsio (2d89f0c8 in master) to production</p>
              </div>
              <time class="flex-shrink-0 ml-3 text-xs text-gray-500 ">5d</time>
            </div>
          </div>
        </section>
      </aside>
    </div>
  </div>
</template>

<script>
export default {
  name: "Home",
  components: {},
  mounted() {
    document.addEventListener("keydown", (e) => {
      if (!this.dropdown || e.key !== "Escape") {
        return;
      }
      this.dropdown = false;
    });
  },
  data: function () {
    return {
      isOpen: false,
      dropdown: false,
    };
  },
  methods: {
    toggleMenu() {
      this.isOpen = !this.isOpen;
    },
    toggleDropdown() {
      this.dropdown = !this.dropdown;
    },
  },
  destroyed() {
    document.removeEventListener("keydown", (e) => {
      if (!this.dropdown || e.key !== "Escape") {
        return;
      }
      this.dropdown = false;
    });
  },
};
</script>
