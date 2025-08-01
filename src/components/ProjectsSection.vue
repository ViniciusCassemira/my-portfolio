<template>
  <section id="projects" class="pt-30">
    <h2 class="text-3xl font-bold text-center text-purple-600">Projects</h2>
    <p class="text-center mb-12">Applications and tools I´ve developed</p>
    <div class="w-full flex justify-center">
      <div class="grid gap-6 sm:grid-cols-1 md:grid-cols-2 lg:grid-cols-3">
        <Project 
        v-for="project in projects" 
        :key="project.id" 
        :title="project.title" 
        :description="project.description" 
        :link="project.link"
        :image="project.image"
        :demo="project.demo"
        :technologies="project.technologies"
        />
      </div>
    </div>
  </section>
</template>

<script>
import Project from './Project.vue'

export default {
  components: { Project },
  data() {
    return {
      projects: [
        {
          id: 1,
          title: 'Javascript Projects',
          description: 'A collection of web applications developed with HTML, CSS, and vanilla JavaScript, showcasing my growth as a front-end developer. Each project is available through a dedicated website or can be run locally via Docker.',
          link: 'https://github.com/ViniciusCassemira/javascript-projects',
          image: '/images/js-projects.png',
          demo: 'https://vinicius-js.netlify.app/',
          technologies: ['html5','css3','javascript']
        },
        {
          id: 2,
          title: 'Docker Essentials',
          description: 'A repository that offers a practical and beginner-friendly guide to Docker. It explains core concepts such as images, containers, volumes, networks, and Docker Compose. The guide includes essential commands and hands-on examples to reinforce learning. Content is organized clearly and progressively to guide users step by step.',
          link: 'https://github.com/ViniciusCassemira/docker-essentials',
          image: '/images/docker.png',
          technologies: ['docker']
        },
        {
          id: 3,
          title: 'Shell Scripts',
          description: '[In development] A collection of scripts interpreted by Unix-like shells, designed to automate common tasks on Debian-based servers. It includes the installation of tools like Nginx, Docker, and Docker Compose, SSH key setup, permission adjustments, and other useful processes for development and production environments.',
          link: 'https://github.com/ViniciusCassemira/shell-scripts',
          image: '/images/shell.png',
          technologies: ['bash']          
        },
        {
          id: 7,
          title: 'Personal Portfolio',
          description: 'My personal portfolio, built with Vue.js and Tailwind CSS, to showcase my projects, skills, and experience as a software developer.',
          link: 'https://github.com/ViniciusCassemira/my-portfolio',
          image: '/images/portfolio.png',
          technologies: ['vuejs','tailwindcss'],
          demo: 'https://cassemira-portfolio.netlify.app'     
        },
        {
          id: 4,
          title: 'Petcare manager',
          description: 'A web application that simulates a pet shop management system. Built with ASP.NET Core MVC and containerized with Docker, it includes features like user registration (admin, vet, client), pet records, appointment scheduling, and management of medications and exams. It also integrates CI/CD workflows using GitHub Actions.'  ,
          link: 'https://github.com/ViniciusCassemira/petcare-manager',
          image: '/images/petcare.png',
          technologies: ['csharp','dotnetcore','bootstrap','docker','githubactions']
        },
        {
          id: 5,
          title: 'PHP MVC Library',
          description: 'A web application built with PHP following the MVC architecture, designed to manage library book reservations. It features user authentication, multilingual support, and distinct interfaces for users and administrators to handle bookings, book data, and user management.',
          link: 'https://github.com/ViniciusCassemira/PHP_MVC_Library',
          image: '/images/library.png',
          technologies: ['css3','javascript','php','mysql','docker']
        },
        {
          id: 6,
          title: 'Benchmark MongoDB',
          description: 'A benchmark project developed during academic studies on NoSQL databases. It involved transforming a relational database into a document-oriented model using MongoDB. The system simulates real-world scenarios of vehicle and traffic violation management, focusing on query performance, indexing strategies, and data modeling. All datasets were artificially generated for educational purposes.',
          link: 'https://github.com/ViniciusCassemira/mongodb-benchmark-detran',
          image: '/images/benchmark.png',
          technologies: ['javascript','mongodb']          
        },
      ]
    }
  }
}
</script>
