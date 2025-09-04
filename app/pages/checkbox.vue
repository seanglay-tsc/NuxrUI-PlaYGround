<script setup lang="ts">
import type { CheckboxGroupItem, CheckboxGroupValue } from '@nuxt/ui'

const items = ref<CheckboxGroupItem[]>([
  {
    label: 'System',
    id: 'system',
  },
  {
    label: 'Light',
    id: 'light',
  },
  {
    label: 'Dark',
    id: 'dark',
  },
])
const value = ref<CheckboxGroupValue[]>([
  'light',
])
</script>

<template>
  <UContainer class="w-full h-screen flex items-center justify-center">
    <UCheckboxGroup v-model="value" value-key="id" :items="items" />
  </UContainer>
</template>
