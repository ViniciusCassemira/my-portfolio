<script setup>
import { ref } from 'vue'

const showMenu = ref(false)

function toggleMenu() {
  showMenu.value = !showMenu.value
}
</script>

<template>
  <section>
    <header class="pt-12 bg-[#050b0e] text-white">
      <nav class="flex items-center justify-between px-8 pt-6">
        <a href="#about" class="font-bold text-xl text-purple-600">./Cassemira</a>

        <!-- Botão hamburguer (aparece em telas pequenas) -->
        <button @click="toggleMenu" class="md:hidden focus:outline-none">
          <svg class="w-6 h-6" fill="none" stroke="currentColor" viewBox="0 0 24 24">
            <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2"
              d="M4 6h16M4 12h16M4 18h16" />
          </svg>
        </button>

        <!-- Menu para telas médias e maiores -->
        <div class="hidden md:flex space-x-10">
          <a href="#experience" class="hover:text-purple-600 text-xl">Experience</a>
          <a href="#technologies" class="hover:text-purple-600 text-xl">Technologies</a>
          <a href="#projects" class="hover:text-purple-600 text-xl">Projetos</a>
          <a href="#contact" class="hover:text-purple-600 text-xl">Contact</a>
        </div>
      </nav>

      <!-- Menu dropdown para telas pequenas -->
      <div v-if="showMenu" class="md:hidden mt-4 px-6 flex flex-col space-y-4">
        <a href="#experience" class="hover:text-purple-600 text-lg">Experience</a>
        <a href="#technologies" class="hover:text-purple-600 text-lg">Technologies</a>
        <a href="#projects" class="hover:text-purple-600 text-lg">Projetos</a>
        <a href="#contact" class="hover:text-purple-600 text-lg">Contact</a>
      </div>
    </header>
  </section>
</template>