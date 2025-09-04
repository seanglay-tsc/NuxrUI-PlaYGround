<script setup lang="ts">
import type { StepperItem } from '@nuxt/ui'

defineProps<{ items: StepperItem[] }>()
const value = defineModel()
</script>

<template>
  <header class="sticky top-0 z-50 border-b bg-white/70 backdrop-blur supports-[backdrop-filter]:bg-white/60">
    <div class="px-6 py-4">
      <UStepper
        v-model="value"
        :items="items"
        :linear="true"
      />
    </div>
  </header>
</template>

onChange
