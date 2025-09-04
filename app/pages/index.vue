<script setup lang="ts">
const links: { to: string, label: string }[] = [
  { to: '/button', label: 'Button' },
  { to: '/checkbox', label: 'Checkbox' },
  { to: '/stepper', label: 'Stepper' },
  { to: '/form', label: 'Form' },
  { to: '/table', label: 'Table' },
  { to: '/calendar', label: 'Calendar' },
]
</script>

<template>
  <div class="h-dvh flex items-center justify-center px-4 md:px-0">
    <ul>
      <li v-for="link in links" :key="link.to">
        <NuxtLink :to="link.to">
          {{ link.label }}
        </NuxtLink>
      </li>
    </ul>
  </div>
</template>
