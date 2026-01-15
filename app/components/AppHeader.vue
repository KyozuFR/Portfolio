<script setup lang="ts">
const navLinks = [
  { label: 'Accueil', href: '/#hero' },
  { label: 'À propos', href: '/#about' },
  { label: 'Compétences', href: '/#skills' },
  { label: 'Projets', href: '/#projects' },
  { label: 'Contact', href: '/#contact' },
]

const isMenuOpen = ref(false)

const closeMenu = () => {
  isMenuOpen.value = false
}
</script>

<template>
  <header class="fixed top-0 left-0 right-0 z-50 bg-primary/95 backdrop-blur-sm border-b border-accent/20">
    <nav class="container mx-auto px-4 py-4 flex items-center justify-between">
      <NuxtLink to="/#hero" class="flex flex-col leading-tight hover:text-secondary transition-colors">
        <span class="text-2xl font-bold text-light">Julien Linares</span>
        <span class="text-xs text-muted">L3 Informatique 7 Recherche stage</span>
      </NuxtLink>

      <!-- Desktop Navigation -->
      <div class="hidden md:flex items-center gap-8">
        <NuxtLink
          v-for="link in navLinks"
          :key="link.href"
          :to="link.href"
          class="text-muted hover:text-secondary transition-colors font-medium"
        >
          {{ link.label }}
        </NuxtLink>
      </div>

      <!-- Mobile Menu Button -->
      <button
        @click="isMenuOpen = !isMenuOpen"
        class="md:hidden text-light hover:text-secondary transition-colors"
        aria-label="Toggle menu"
      >
        <Icon :name="isMenuOpen ? 'heroicons:x-mark' : 'heroicons:bars-3'" class="w-6 h-6" />
      </button>
    </nav>

    <!-- Mobile Navigation -->
    <div
      v-show="isMenuOpen"
      class="md:hidden bg-primary border-t border-accent/20"
    >
      <nav class="container mx-auto px-4 py-4 flex flex-col gap-4">
        <NuxtLink
          v-for="link in navLinks"
          :key="link.href"
          :to="link.href"
          class="block text-muted hover:text-secondary transition-colors font-medium py-2"
          @click="closeMenu"
        >
          {{ link.label }}
        </NuxtLink>
      </nav>
    </div>
  </header>
</template>

<style scoped>

</style>