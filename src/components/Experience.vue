<template>
  <div class="project-card border rounded-2xl overflow-hidden shadow-lg max-w-sm">
    <div class="p-4">
      <h3 class="text-xl font-semibold mb-2">{{ title }}</h3>
      <div class="flex justify-between">
          <a :href="url" target="_blank" class="text-gray-600 mb-4 inline-flex items-center gap-1">
            {{ enterprise }}
            <ArrowTopRightOnSquareIcon class="w-4 h-4 text-gray-400" />
          </a>
          <p class="text-gray-600 mb-4">{{ period }}</p>
        </div>
      <p> {{ description }}</p>
    </div>
  </div>
</template>

<script>
import { ArrowTopRightOnSquareIcon } from '@heroicons/vue/24/outline'
export default {
  props: {
    title: String,
    enterprise: String,
    url: String,
    period: String,
    description: String
  },
  components: {
    ArrowTopRightOnSquareIcon
  }
}
</script>