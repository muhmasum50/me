<script setup lang="ts">
const focus = [
  { tag: 'backend', text: 'APIs, business logic, databases, and system architecture.' },
  { tag: 'full-stack', text: 'Building applications from backend to frontend.' },
  { tag: 'devops', text: 'Docker, CI/CD, deployment automation, and infrastructure.' },
  { tag: 'security & quality', text: 'Security scanning, code analysis, secure development practices.' },
  { tag: 'monitoring & reliability', text: 'Observability and maintaining reliable applications.', wide: true }
]
</script>

<template>
  <section
    id="what-i-do"
    class="px-6 py-20 border-t border-default"
  >
    <UContainer class="max-w-3xl">
      <p class="font-mono text-xs text-muted mb-2">
        03 / FOCUS
      </p>
      <h2 class="text-2xl font-semibold font-mono mb-8">
        What I Do
      </h2>
      <div class="grid sm:grid-cols-2 gap-4">
        <UCard
          v-for="item in focus"
          :key="item.tag"
          :class="item.wide ? 'sm:col-span-2' : ''"
          :ui="{ body: 'p-5' }"
        >
          <p class="font-mono text-xs text-muted mb-2">
            {{ item.tag }}
          </p>
          <p class="text-sm">
            {{ item.text }}
          </p>
        </UCard>
      </div>
    </UContainer>
  </section>
</template>
