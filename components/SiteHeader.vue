<template>
  <header data-fetch-key="1" class="relative w-full mx-auto bg-white px-8">

    <div class="max-w-screen-xl mx-auto">
      <div class="flex justify-between items-center py-6 md:justify-start md:space-x-10">
        <div class="lg:w-0 lg:flex-1">
          <a href="/" class="flex items-center">
            <img
              v-if="logo"
              :src="logo"
              alt="My Travel Blog"
              title="My Travel Blog"
              class="h-14 sm:h-20 w-auto z-50"
            />

            <img
              v-else
              src="https://cdn.aglty.io/blog-starter-2021-template/logos/travel-blog-logo.png"
              alt="My Travel Blog"
              title="My Travel Blog"
              class="h-14 sm:h-20 w-auto z-50"
            />
            <p
              v-if="title !== undefined"
              class="font-bold text-4xl text-secondary-500 ml-3 mt-2"
            >
              {{ title }}
            </p></a
          >
        </div>
        <div class="-mr-2 -my-2 md:hidden">
          <button
            type="button"
            class="inline-flex items-center justify-center p-2 rounded-md text-gray-400 hover:text-gray-500 hover:bg-gray-100 focus:outline-none focus:bg-gray-100 focus:text-gray-500 transition duration-150 ease-in-out"
          >
            <svg
              xmlns="http://www.w3.org/2000/svg"
              fill="none"
              viewBox="0 0 24 24"
              stroke="currentColor"
              class="h-6 w-6"
            >
              <path
                strokelinecap="round"
                strokelinejoin="round"
                strokewidth="2"
                d="M4 6h16M4 12h16M4 18h16"
              ></path>
            </svg>
          </button>
        </div>
        <nav class="hidden md:flex space-x-10">
          <nuxt-link
            to="/"
            class="text-base leading-6 font-medium text-secondary-500 hover:text-green-500 border-transparent border-b-2 hover:border-red-200 hover:border-b-primary hover:border-b-2 focus:outline-none focus:text-primary-500 transition duration-300"
          >
            Home </nuxt-link
          ><nuxt-link
            to="/blog"
            class="text-base leading-6 font-medium text-secondary-500 hover:text-green-500 border-transparent border-b-2 hover:border-red-200 hover:border-b-primary hover:border-b-2 focus:outline-none focus:text-primary-500 transition duration-300"
          >
            Blog </nuxt-link
          ><nuxt-link
            to="/about"
            class="text-base leading-6 font-medium text-secondary-500 hover:text-green-500 border-transparent border-b-2 hover:border-red-200 hover:border-b-primary hover:border-b-2 focus:outline-none focus:text-primary-500 transition duration-300"
          >
            About
          </nuxt-link>
        </nav>
      </div>
    </div>
    <div
      class="absolute top-0 inset-x-0 p-2 transition transform origin-top-right md:hidden z-20"
      style="display: none"
    >
      <div class="rounded-lg shadow-lg">
        <div class="rounded-lg shadow-xs bg-white divide-y-2 divide-gray-50">
          <div class="pt-5 pb-6 px-5 space-y-6">
            <div class="flex items-center justify-end">
              <div class="-mr-2">
                <button
                  aria-label="Toggle Menu"
                  type="button"
                  class="inline-flex items-center justify-center p-2 rounded-md text-gray-400 hover:text-gray-500 hover:bg-gray-100 focus:outline-none focus:bg-gray-100 focus:text-gray-500 transition duration-300"
                >
                  <svg
                    xmlns="http://www.w3.org/2000/svg"
                    fill="none"
                    viewBox="0 0 24 24"
                    stroke="currentColor"
                    class="h-6 w-6"
                  >
                    <path
                      strokelinecap="round"
                      strokelinejoin="round"
                      strokewidth="2"
                      d="M6 18L18 6M6 6l12 12"
                    ></path>
                  </svg>
                </button>
              </div>
            </div>
            <div>
              <nav class="grid gap-y-8">
                <a
                  href="/home"
                  class="-m-3 p-3 flex items-center space-x-3 rounded-md hover:bg-gray-50 transition duration-300"
                  ><svg
                    xmlns="http://www.w3.org/2000/svg"
                    fill="none"
                    viewBox="0 0 24 24"
                    stroke="currentColor"
                    class="flex-shrink-0 h-6 w-6 text-primary-600"
                  >
                    <path
                      strokelinecap="round"
                      strokelinejoin="round"
                      strokewidth="2"
                      d="M4 6a2 2 0 012-2h2a2 2 0 012 2v2a2 2 0 01-2 2H6a2 2 0 01-2-2V6zM14 6a2 2 0 012-2h2a2 2 0 012 2v2a2 2 0 01-2 2h-2a2 2 0 01-2-2V6zM4 16a2 2 0 012-2h2a2 2 0 012 2v2a2 2 0 01-2 2H6a2 2 0 01-2-2v-2zM14 16a2 2 0 012-2h2a2 2 0 012 2v2a2 2 0 01-2 2h-2a2 2 0 01-2-2v-2z"
                    ></path>
                  </svg>
                  <div class="text-base leading-6 font-medium text-gray-900">Home</div></a
                ><a
                  href="/blog"
                  class="-m-3 p-3 flex items-center space-x-3 rounded-md hover:bg-gray-50 transition duration-300"
                  ><svg
                    xmlns="http://www.w3.org/2000/svg"
                    fill="none"
                    viewBox="0 0 24 24"
                    stroke="currentColor"
                    class="flex-shrink-0 h-6 w-6 text-primary-600"
                  >
                    <path
                      strokelinecap="round"
                      strokelinejoin="round"
                      strokewidth="2"
                      d="M4 6a2 2 0 012-2h2a2 2 0 012 2v2a2 2 0 01-2 2H6a2 2 0 01-2-2V6zM14 6a2 2 0 012-2h2a2 2 0 012 2v2a2 2 0 01-2 2h-2a2 2 0 01-2-2V6zM4 16a2 2 0 012-2h2a2 2 0 012 2v2a2 2 0 01-2 2H6a2 2 0 01-2-2v-2zM14 16a2 2 0 012-2h2a2 2 0 012 2v2a2 2 0 01-2 2h-2a2 2 0 01-2-2v-2z"
                    ></path>
                  </svg>
                  <div class="text-base leading-6 font-medium text-gray-900">Blog</div></a
                ><a
                  href="/about"
                  class="-m-3 p-3 flex items-center space-x-3 rounded-md hover:bg-gray-50 transition duration-300"
                  ><svg
                    xmlns="http://www.w3.org/2000/svg"
                    fill="none"
                    viewBox="0 0 24 24"
                    stroke="currentColor"
                    class="flex-shrink-0 h-6 w-6 text-primary-600"
                  >
                    <path
                      strokelinecap="round"
                      strokelinejoin="round"
                      strokewidth="2"
                      d="M4 6a2 2 0 012-2h2a2 2 0 012 2v2a2 2 0 01-2 2H6a2 2 0 01-2-2V6zM14 6a2 2 0 012-2h2a2 2 0 012 2v2a2 2 0 01-2 2h-2a2 2 0 01-2-2V6zM4 16a2 2 0 012-2h2a2 2 0 012 2v2a2 2 0 01-2 2H6a2 2 0 01-2-2v-2zM14 16a2 2 0 012-2h2a2 2 0 012 2v2a2 2 0 01-2 2h-2a2 2 0 01-2-2v-2z"
                    ></path>
                  </svg>
                  <div class="text-base leading-6 font-medium text-gray-900">
                    About
                  </div></a
                >
              </nav>
            </div>
          </div>
        </div>
      </div>
    </div>
  </header>
</template>

<script>
export default {
  data() {
    return {
      title: "",
      logo: "",
    };
  },
  mounted() {
    this.title = this.$store.state.siteconfigs.siteconfigs[0].content.body[0].title;
    this.logo = this.$store.state.siteconfigs.siteconfigs[0].content.body[0].logo[0].link.url;
  },
};
</script>
