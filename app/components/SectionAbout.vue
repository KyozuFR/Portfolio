<script setup lang="ts">

</script>

<template>
  <section id="about" class="py-20 bg-light">
    <div class="container mx-auto px-4">
      <h2 class="text-3xl md:text-4xl font-bold text-primary text-center mb-12">
        À propos de moi
      </h2>

      <div class="max-w-4xl mx-auto grid md:grid-cols-2 gap-12 items-center">
        <!-- Photo placeholder -->
        <div class="flex justify-center">
          <div class="w-64 h-64 rounded-full bg-gradient-to-br from-secondary to-accent flex items-center justify-center">
            <Icon name="heroicons:user" class="w-32 h-32 text-light" />
          </div>
        </div>

        <!-- Description -->
        <div>
          <p class="text-primary/80 text-lg leading-relaxed mb-6">
            Je suis étudiant en <strong>L3 Informatique</strong> (parcours international La Rochelle Université &amp; University of Galway). J’ai une base solide en programmation orientée objet (Java, PHP) et en développement web (Symfony, Vue.js).
          </p>
          <p class="text-primary/80 text-lg leading-relaxed mb-6">
            En parallèle de mes études, j’ai déjà mené des <strong>projets freelance</strong> (sites vitrines, application de gestion clients). J’aime livrer des fonctionnalités propres et maintenables, en faisant attention à l’expérience utilisateur, à la qualité du code et aux bonnes pratiques.
          </p>
          <p class="text-primary/80 text-lg leading-relaxed">
            Aujourd’hui, je cherche un <strong>stage de fin de licence</strong>. Je m’oriente naturellement vers le <strong>développement</strong>, mais je m’intéresse aussi à l’<strong>infra &amp; réseau</strong> (systèmes, protocoles) — l’objectif est de trouver un environnement où je peux explorer ces deux axes et monter en compétence.
          </p>
        </div>
      </div>
    </div>
  </section>
</template>

<style scoped>

</style>
