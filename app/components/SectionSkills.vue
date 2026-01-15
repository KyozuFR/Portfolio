<script setup lang="ts">
const skillCategories = [
  {
    title: 'Développement web',
    icon: 'heroicons:code-bracket',
    skills: ['Vue.js', 'Nuxt', 'Symfony', 'HTML/CSS', 'JavaScript/TypeScript (bases)']
  },
  {
    title: 'Programmation',
    icon: 'heroicons:cpu-chip',
    skills: ['Programmation orientée objet (Java, PHP)', 'Programmation impérative (C)', 'Conception & structuration du code']
  },
  {
    title: 'Systèmes & réseau',
    icon: 'heroicons:server-stack',
    skills: ['Réseau & protocoles', "Systèmes d’exploitation", 'Bases Linux', 'Notions CI/CD & tests']
  },
  {
    title: 'Outils & méthodes',
    icon: 'heroicons:wrench-screwdriver',
    skills: ['Git', 'Gestion de projet', 'Travail en autonomie', 'Documentation']
  }
]
</script>

<template>
  <section id="skills" class="py-20 bg-primary">
    <div class="container mx-auto px-4">
      <h2 class="text-3xl md:text-4xl font-bold text-light text-center mb-12">
        Mes compétences
      </h2>

      <div class="grid md:grid-cols-2 lg:grid-cols-4 gap-8 max-w-6xl mx-auto">
        <div
          v-for="category in skillCategories"
          :key="category.title"
          class="bg-primary border border-accent/30 rounded-2xl p-6 hover:border-secondary transition-colors"
        >
          <div class="flex items-center gap-3 mb-6">
            <div class="w-12 h-12 rounded-lg bg-secondary/20 flex items-center justify-center">
              <Icon :name="category.icon" class="w-6 h-6 text-secondary" />
            </div>
            <h3 class="text-xl font-semibold text-light">{{ category.title }}</h3>
          </div>

          <ul class="space-y-3">
            <li
              v-for="skill in category.skills"
              :key="skill"
              class="flex items-center gap-2 text-muted"
            >
              <Icon name="heroicons:check-circle" class="w-5 h-5 text-accent" />
              {{ skill }}
            </li>
          </ul>
        </div>
      </div>

      <div class="max-w-6xl mx-auto mt-12 grid md:grid-cols-2 gap-8">
        <div class="bg-primary border border-accent/30 rounded-2xl p-6">
          <h3 class="text-xl font-semibold text-light mb-4">Langues</h3>
          <ul class="space-y-3">
            <li class="flex items-center gap-2 text-muted">
              <Icon name="heroicons:check-circle" class="w-5 h-5 text-accent" />
              Français
            </li>
            <li class="flex items-center gap-2 text-muted">
              <Icon name="heroicons:check-circle" class="w-5 h-5 text-accent" />
              Anglais
            </li>
          </ul>
        </div>

        <div class="bg-primary border border-accent/30 rounded-2xl p-6">
          <h3 class="text-xl font-semibold text-light mb-4">Intérêts</h3>
          <ul class="space-y-3">
            <li class="flex items-center gap-2 text-muted">
              <Icon name="heroicons:check-circle" class="w-5 h-5 text-accent" />
              Développement informatique
            </li>
            <li class="flex items-center gap-2 text-muted">
              <Icon name="heroicons:check-circle" class="w-5 h-5 text-accent" />
              Randonnée en autonomie
            </li>
            <li class="flex items-center gap-2 text-muted">
              <Icon name="heroicons:check-circle" class="w-5 h-5 text-accent" />
              Prises de vue aériennes
            </li>
          </ul>
        </div>
      </div>
    </div>
  </section>
</template>

<style scoped>
</style>
