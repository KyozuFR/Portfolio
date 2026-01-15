<script setup lang="ts">
const currentYear = new Date().getFullYear()

const socialLinks = [
  { name: 'GitHub', icon: 'mdi:github', href: 'https://github.com/' },
  { name: 'LinkedIn', icon: 'mdi:linkedin', href: 'https://www.linkedin.com/' },
  { name: 'Site', icon: 'heroicons:globe-alt', href: 'https://2linares.fr' },
]
</script>

<template>
  <footer class="py-8 bg-primary border-t border-accent/20">
    <div class="container mx-auto px-4">
      <div class="flex flex-col md:flex-row items-center justify-between gap-4">
        <p class="text-muted text-sm">© {{ currentYear }} Julien Linares · Portfolio</p>

        <div class="flex items-center gap-4">
          <a
            v-for="social in socialLinks"
            :key="social.name"
            :href="social.href"
            :aria-label="social.name"
            class="text-muted hover:text-secondary transition-colors"
          >
            <Icon :name="social.icon" class="w-5 h-5" />
          </a>
        </div>

        <a
          href="#hero"
          class="flex items-center gap-1 text-muted hover:text-secondary transition-colors text-sm"
        >
          Retour en haut
          <Icon name="heroicons:arrow-up" class="w-4 h-4" />
        </a>
      </div>
    </div>
  </footer>
</template>

<style scoped>
</style>
