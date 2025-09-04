<script setup lang="ts">
const props = defineProps<{ total: number }>()
const currentStep = defineModel<number>({ default: 1 })
function prev() {
  if (currentStep.value > 0)
    currentStep.value--
}

function next() {
  if (currentStep.value < props.total - 1)
    currentStep.value++
}
</script>

<template>
  <footer class="sticky bottom-0 z-50 border-t bg-white/70 backdrop-blur supports-[backdrop-filter]:bg-white/60">
    <div class="mx-auto flex w-full max-w-5xl justify-between gap-4 p-4">
      <UButton leading-icon="i-lucide-arrow-left" :disabled="currentStep === 0" @click="prev">
        Prev
      </UButton>

      <UButton trailing-icon="i-lucide-arrow-right" :disabled="currentStep === props.total - 1" @click="next">
        Next
      </UButton>
    </div>
  </footer>
</template>
