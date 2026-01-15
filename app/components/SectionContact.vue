<script setup lang="ts">
const form = reactive({
  name: '',
  email: '',
  message: ''
})

const handleSubmit = () => {
  // Logique d'envoi du formulaire
  console.log('Form submitted:', form)
}

const socialLinks = [
  { name: 'GitHub', icon: 'mdi:github', href: 'https://github.com/' },
  { name: 'LinkedIn', icon: 'mdi:linkedin', href: 'https://www.linkedin.com/' },
  { name: 'Site', icon: 'heroicons:globe-alt', href: 'https://2linares.fr' },
]
</script>

<template>
  <section id="contact" class="py-20 bg-primary">
    <div class="container mx-auto px-4">
      <h2 class="text-3xl md:text-4xl font-bold text-light text-center mb-12">
        Me contacter
      </h2>

      <div class="max-w-4xl mx-auto grid md:grid-cols-2 gap-12">
        <!-- Contact Info -->
        <div>
          <h3 class="text-2xl font-semibold text-light mb-6">Discutons d’un stage / d’une alternance</h3>
          <p class="text-muted mb-8">
            Je recherche un <strong>stage de fin de licence</strong>. Si vous avez un sujet (développement web, back-end, qualité/CI-CD, ou même infra/réseau), je serai ravi d’échanger.
          </p>

          <div class="space-y-4 mb-8">
            <div class="flex items-center gap-3 text-muted">
              <Icon name="heroicons:envelope" class="w-5 h-5 text-secondary" />
              <a href="mailto:julien@2linares.fr" class="hover:text-secondary transition-colors">
                julien@2linares.fr
              </a>
            </div>
            <div class="flex items-center gap-3 text-muted">
              <Icon name="heroicons:globe-alt" class="w-5 h-5 text-secondary" />
              <a href="https://2linares.fr" class="hover:text-secondary transition-colors">
                2linares.fr
              </a>
            </div>
          </div>

          <!-- Social Links -->
          <div class="flex gap-4">
            <a
              v-for="social in socialLinks"
              :key="social.name"
              :href="social.href"
              :aria-label="social.name"
              class="w-10 h-10 rounded-full bg-accent/20 flex items-center justify-center text-muted hover:bg-secondary hover:text-light transition-colors"
            >
              <Icon :name="social.icon" class="w-5 h-5" />
            </a>
          </div>
        </div>

        <!-- Contact Form -->
        <form @submit.prevent="handleSubmit" class="space-y-6">
          <div>
            <label for="name" class="block text-muted mb-2">Nom</label>
            <input
              id="name"
              v-model="form.name"
              type="text"
              required
              class="w-full px-4 py-3 rounded-lg bg-primary border border-accent/30 text-light placeholder-muted/50 focus:border-secondary focus:outline-none transition-colors"
              placeholder="Votre nom"
            >
          </div>

          <div>
            <label for="email" class="block text-muted mb-2">Email</label>
            <input
              id="email"
              v-model="form.email"
              type="email"
              required
              class="w-full px-4 py-3 rounded-lg bg-primary border border-accent/30 text-light placeholder-muted/50 focus:border-secondary focus:outline-none transition-colors"
              placeholder="votre@email.com"
            >
          </div>

          <div>
            <label for="message" class="block text-muted mb-2">Message</label>
            <textarea
              id="message"
              v-model="form.message"
              rows="5"
              required
              class="w-full px-4 py-3 rounded-lg bg-primary border border-accent/30 text-light placeholder-muted/50 focus:border-secondary focus:outline-none transition-colors resize-none"
              placeholder="Votre message..."
            ></textarea>
          </div>

          <button
            type="submit"
            class="w-full px-8 py-3 bg-secondary text-light rounded-lg font-semibold hover:bg-accent transition-colors"
          >
            Envoyer
          </button>
          <p class="text-xs text-muted">
            (Le formulaire ne fait pas encore d’envoi automatique — il sert de brouillon. Je peux le connecter à un service d’email ensuite.)
          </p>
        </form>
      </div>
    </div>
  </section>
</template>

<style scoped>
</style>
