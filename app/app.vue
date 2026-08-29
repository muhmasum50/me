<script setup>
useHead({
  meta: [
    { name: 'viewport', content: 'width=device-width, initial-scale=1' }
  ],
  link: [
    { rel: 'icon', href: '/favicon.ico' }
  ],
  htmlAttrs: {
    lang: 'en'
  }
})

const title = 'Me'
const description = 'Profile'

useSeoMeta({
  title,
  description,
  ogTitle: title,
  ogDescription: description,
  ogImage: 'https://ui.nuxt.com/assets/templates/nuxt/starter-light.png',
  twitterCard: 'summary_large_image'
})
</script>

<template>
  <div class="page-bg">
    <TheHeader />
    <HeroSection />
    <AboutSection />
    <StackSection />
    <FocusSection />
    <ContactSection />
    <USeparator icon="i-simple-icons-nuxtdotjs" />
    <TheFooter />
  </div>
</template>
