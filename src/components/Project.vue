<template>
  <div class="project-card group border-2 overflow-hidden shadow-lg max-w-sm hover:border-purple-600 transition flex flex-col">
    <img :src="image" :alt="title" class="w-full h-50 object-cover" />
    <div class="p-4 flex flex-col justify-between flex-1">
      <div>
        <div class="flex justify-between">
          <h3 class="text-xl font-semibold mb-2 text-[#ececec]">{{ title }}</h3>
          <div class="flex gap-1.5">
            <i v-for="(tech, index) in technologies" :key="index" :class="`devicon-${tech}-plain colored text-2xl`"></i>
          </div>
        </div>
        <p class="text-gray-600 mb-4">{{ description }}</p>
      </div>
      <div class="flex gap-2 mt-auto">
        <a :href="link" target="_blank"
           class="inline-block text-white bg-gray-600 group-hover:bg-purple-600 px-4 py-2 rounded-md transition">
          View details
        </a>
        <a v-if="demo" :href="demo" target="_blank"
           class="inline-block text-white bg-green-600 hover:bg-green-700 px-4 py-2 rounded-md transition">
          Demo
        </a>
      </div>
    </div>
  </div>
</template>

<script>
//import { ArrowTopRightOnSquareIcon } from '@heroicons/vue/24/outline'
export default {
  props: {
    title: String,
    description: String,
    link: String,
    image: String,
    demo: String,
    technologies: Array
  }
}
</script>