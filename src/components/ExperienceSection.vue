<template>
  <section id="experience" class="pt-30">
    <h2 class="text-3xl font-bold mb-7 text-center text-purple-600">Professional Experience</h2>
    <div class="w-full flex justify-center">
      <div class="grid grid-cols-1 gap-6">
        <ExperienceCard v-for="experience in experiences" :key="experience.id" :title="experience.title"
          :enterprise="experience.enterprise" :url="experience.url" :period="experience.period" :description="experience.description" />
      </div>
    </div>
  </section>
</template>

<script>
import ExperienceCard from './Experience.vue' // Nome do componente que você criou

export default {
  components: {
    ExperienceCard
  },
  data() {
    return {
      experiences: [
        {
          id: 1,
          title: 'DevOps Intern',
          enterprise: 'Labi9',
          url: 'https://labi9.com',
          period: 'Oct 2024 - Present',
          description: 'I work in the development of CI/CD pipelines, infrastructure automation and provisioning, systems monitoring and support tasks.'
        }
      ]
    }
  }
}
</script>
