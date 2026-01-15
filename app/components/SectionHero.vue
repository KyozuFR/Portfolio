<script setup lang="ts">

</script>

<template>
  <section id="hero" class="min-h-screen flex items-center justify-center bg-primary pt-16">
    <div class="container mx-auto px-4 text-center">
      <div class="max-w-3xl mx-auto">
        <h1 class="text-4xl md:text-6xl font-bold text-light mb-6">
          Bonjour, je suis
          <span class="text-secondary">Julien Linares</span>
        </h1>
        <p class="text-xl md:text-2xl text-muted mb-4">
          Étudiant en <span class="text-light font-semibold">L3 Informatique</span> — je cherche un <span class="text-light font-semibold">stage de fin de licence</span>.
        </p>
        <p class="text-lg md:text-xl text-muted mb-8">
          À l’aise en <span class="text-light font-semibold">développement web</span> (Vue.js, Symfony) et curieux côté <span class="text-light font-semibold">infra & réseau</span> (systèmes, protocoles). Je veux rejoindre une équipe technique et progresser sur l’industrialisation (tests, CI/CD).
        </p>
        <div class="flex flex-col sm:flex-row gap-4 justify-center">
          <a
            href="#projects"
            class="px-8 py-3 bg-secondary text-light rounded-lg font-semibold hover:bg-accent transition-colors"
          >
            Voir mes projets
          </a>
          <a
            href="#contact"
            class="px-8 py-3 border-2 border-secondary text-secondary rounded-lg font-semibold hover:bg-secondary hover:text-light transition-colors"
          >
            Me contacter
          </a>
        </div>
      </div>

      <!-- Scroll indicator -->
      <div class="absolute bottom-8 left-1/2 -translate-x-1/2 animate-bounce">
        <Icon name="heroicons:chevron-down" class="w-8 h-8 text-muted" />
      </div>
    </div>
  </section>
</template>

<style scoped>

</style>
