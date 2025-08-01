<script setup>
import { ref } from 'vue'
import HeaderSection from './components/HeaderSection.vue'
import AboutSection from './components/AboutSection.vue'
import ProjectsSection from './components/ProjectsSection.vue'
import ContactSection from './components/ContactSection.vue'
import ExperienceSection from './components/ExperienceSection.vue'
import TechnologiesSection from './components/TechnologiesSection.vue'

const text = ref("")
const message = ref(false)
const greeting = ref('Hello from parent')

function toggle(){
  message.value = !message.value;
}
</script>

<template>
  <div class="bg-[#050b0e] text-[#ececec] font-rubik">

    <HeaderSection />
    <AboutSection />
    <ExperienceSection />
    <TechnologiesSection />
    <ProjectsSection />
    <ContactSection />
  </div>
</template>