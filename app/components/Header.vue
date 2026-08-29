<template>
  <header class="fixed top-0 inset-x-0 z-50 backdrop-blur border-b border-default bg-(--ui-bg)/80">
    <UContainer class="max-w-4xl flex items-center justify-between py-4">
      <a href="#" class="font-mono text-sm">Ma'sum<span class="cursor-blink" /></a>
      <div class="flex items-center gap-6">
        <nav class="hidden sm:flex gap-6 font-mono text-xs text-muted">
          <a href="#about" class="hover:text-default transition">about</a>
          <a href="#stack" class="hover:text-default transition">stack</a>
          <a href="#what-i-do" class="hover:text-default transition">what-i-do</a>
          <a href="#contact" class="hover:text-default transition">contact</a>
        </nav>
        <ClientOnly>
          <UButton
            :icon="icons[colorMode.preference as keyof typeof icons] ?? icons.system"
            variant="ghost"
            color="neutral"
            size="xs"
            :aria-label="`Theme: ${colorMode.preference}`"
            @click="cycleTheme"
          />
          <template #fallback>
            <div class="size-8" />
          </template>
        </ClientOnly>
      </div>
    </UContainer>
  </header>
</template>

<script setup lang="ts">
const colorMode = useColorMode()

const icons = { light: 'i-lucide-sun', dark: 'i-lucide-moon', system: 'i-lucide-monitor' }
const order = ['system', 'light', 'dark'] as const

function cycleTheme() {
  const idx = order.indexOf(colorMode.preference as typeof order[number])
  colorMode.preference = order[(idx + 1) % order.length]
}
</script>

