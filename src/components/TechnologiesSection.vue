<template>
  <section id="technologies" class="text-center pt-30">
    <h2 class="text-3xl font-bold text-purple-600">Technologies e Tools</h2>
    <p class="mb-8">I’m experienced with and use regularly:</p>
    <div class="overflow-hidden w-full py-4">
      <h2 class="text-left text-xl pl-8">Languages and databases</h2>
      <div class="scroll-wrapper mb-6">
        <div class="scroll-track">
          <div v-for="(icon, i) in duplicatedIcons" :key="i" class="w-12 h-12 mx-25 flex-shrink-0">
            <img :src="icon" alt="icon" class="w-full h-full" />
          </div>
        </div>
      </div>

      <h2 class="text-left text-xl pl-8">Cloud & Deployment</h2>
      <div class="scroll-wrapper mb-6">
        <div class="scroll-track2">
          <div v-for="(icon, i) in duplicatedIcons2" :key="i" class="w-12 h-12 mx-20 flex-shrink-0">
            <img :src="icon" alt="icon" class="w-full h-full" />
          </div>
        </div>
      </div>

      <h2 class="text-left text-xl pl-8">Tools & DevOps</h2>
      <div class="scroll-wrapper mb-6">
        <div class="scroll-track3">
          <div v-for="(icon, i) in duplicatedIcons3" :key="i" class="w-12 h-12 mx-30 flex-shrink-0">
            <img :src="icon" alt="icon" class="w-full h-full" />
          </div>
        </div>
      </div>
    </div>
  </section>
</template>

<script setup>
const icons = [
  '/src/assets/tech/javascript.svg',
  '/src/assets/tech/mongo.svg',
  '/src/assets/tech/mysql.svg',
  '/src/assets/tech/java.svg',
  '/src/assets/tech/python.svg',
  '/src/assets/tech/csharp.svg'
]
const icons2 = [
  '/src/assets/tech/heroku.svg',
  '/src/assets/tech/aws.svg',
  '/src/assets/tech/digitalocean.svg',
  '/src/assets/tech/netlify.svg',
  '/src/assets/tech/cloudflare.svg'
]
const icons3 = [
  '/src/assets/tech/docker.svg',
  '/src/assets/tech/github.svg',
  '/src/assets/tech/gitlab.svg',
  '/src/assets/tech/linux.svg'
]

const duplicatedIcons = [...icons, ...icons, ...icons, ...icons]
const duplicatedIcons2 = [...icons2, ...icons2, ...icons2, ...icons2]
const duplicatedIcons3 = [...icons3, ...icons3, ...icons3, ...icons3]
</script>

<style scoped>
.scroll-wrapper {
  width: 100%;
  overflow: hidden;
  position: relative;
}

@keyframes scroll-left {
  0% {
    transform: translateX(0);
  }

  100% {
    transform: translateX(-50%);
  }
}

@keyframes scroll-right {
  0% {
    transform: translateX(-50%);
  }

  100% {
    transform: translateX(0);
  }
}

.scroll-track {
  display: flex;
  width: max-content;
  animation: scroll-left 10s linear infinite;
}

.scroll-track2 {
  display: flex;
  width: max-content;
  animation: scroll-right 10s linear infinite;
}

.scroll-track3 {
  display: flex;
  width: max-content;
  animation: scroll-left 12s linear infinite;
}
</style>