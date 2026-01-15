<script setup lang="ts">
type Project = {
  title: string
  description: string
  technologies: string[]
  link?: string
  github?: string
}

const projects: Project[] = [
  {
    title: 'Solution de gestion clients (Symfony)',
    description:
        "Application web de gestion clients et stockage de données : interface d’administration, gestion des utilisateurs et persistance en base de données.",
    technologies: ['Symfony', 'PHP', 'Base de données', 'Auth / rôles'],
    image: null,
    link: '#',
    github: '#'
  },
  {
    title: 'Sites vitrines pour PME (freelance)',
    description:
      'Création et mise en ligne de sites vitrines : pages responsives, contenu administrable (selon besoin) et bonnes pratiques de performance.',
    technologies: ['Vue.js', 'HTML/CSS', 'Déploiement'],
  },
  {
    title: 'Projets académiques (POO / C / réseau)',
    description:
      'Travaux pratiques et projets de licence : programmation orientée objet (Java/PHP), programmation impérative (C) et notions réseau/systèmes.',
    technologies: ['Java', 'PHP', 'C', 'Réseau & systèmes'],
  },
]
</script>

<template>
  <section id="projects" class="py-20 bg-light">
    <div class="container mx-auto px-4">
      <h2 class="text-3xl md:text-4xl font-bold text-primary text-center mb-12">
        Mes projets
      </h2>

      <div class="grid md:grid-cols-2 lg:grid-cols-3 gap-8 max-w-6xl mx-auto">
        <article
          v-for="project in projects"
          :key="project.title"
          class="bg-white rounded-2xl overflow-hidden shadow-lg hover:shadow-xl transition-shadow border border-muted/30"
        >
          <!-- Image placeholder -->
          <div class="h-48 bg-gradient-to-br from-secondary/20 to-accent/20 flex items-center justify-center">
            <Icon name="heroicons:code-bracket-square" class="w-16 h-16 text-accent" />
          </div>

          <div class="p-6">
            <h3 class="text-xl font-semibold text-primary mb-2">{{ project.title }}</h3>
            <p class="text-primary/70 mb-4">{{ project.description }}</p>

            <!-- Technologies -->
            <div class="flex flex-wrap gap-2 mb-4">
              <span
                v-for="tech in project.technologies"
                :key="tech"
                class="px-3 py-1 bg-accent/20 text-accent text-sm rounded-full"
              >
                {{ tech }}
              </span>
            </div>

            <!-- Links (optionnels) -->
            <div class="flex gap-4" v-if="project.link || project.github">
              <a
                v-if="project.link"
                :href="project.link"
                class="flex items-center gap-1 text-secondary hover:text-accent transition-colors"
              >
                <Icon name="heroicons:arrow-top-right-on-square" class="w-4 h-4" />
                Voir le site
              </a>
              <a
                v-if="project.github"
                :href="project.github"
                class="flex items-center gap-1 text-secondary hover:text-accent transition-colors"
              >
                <Icon name="mdi:github" class="w-4 h-4" />
                GitHub
              </a>
            </div>
          </div>
        </article>
      </div>

      <p class="text-center text-primary/60 mt-10">
        Je peux partager plus de contexte (captures, code, détails techniques) sur demande.
      </p>
    </div>
  </section>
</template>

<style scoped>
</style>
