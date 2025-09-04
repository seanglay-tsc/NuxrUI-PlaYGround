<script setup lang="ts">
import type { StepperItem } from '@nuxt/ui'
import { ref } from 'vue'

const items: StepperItem[] = [
  { title: 'Address', description: 'Add your address here', icon: 'i-lucide-house' },
  { title: 'Shipping', description: 'Set your preferred shipping method', icon: 'i-lucide-truck' },
  { title: 'Checkout', description: 'Confirm your order' },
]
const current = ref(0)
</script>

<template>
  <div class="flex h-screen flex-col">
    <StepperHeader v-model="current" :items="items" />
    <StepperContent :items="items" :current="current" :count="20" />
    <StepperFooter v-model="current" :total="items.length" />
  </div>
</template>
