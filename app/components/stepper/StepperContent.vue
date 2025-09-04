<script setup lang="ts">
import type { StepperItem } from '@nuxt/ui'

const props = withDefaults(defineProps<{
  items: StepperItem[]
  current: number
  count?: number
}>(), { count: 20 })
</script>

<template>
  <main class="flex-1 overflow-y-auto px-8 py-8">
    <div class="grid grid-cols-2 gap-4">
      <div v-for="n in props.count" :key="n" class="aspect-video flex items-center justify-center">
        {{ props.items[props.current].title }} #{{ n }}
      </div>
    </div>
  </main>
</template>
