<script setup lang="ts">
const { data, status, error, execute } = await useFetch('https://jsonplaceholder.typicode.com/posts', {
  key: 'posts',
  immediate: false,
})
</script>

<template>
  <UContainer>
    <UButton @click="execute">
      fetch meow
    </UButton>
    <div v-if="status === 'pending'">
      Loading ...
    </div>
    <div v-if="status === 'error'">
      {{ error }}
    </div>
    <UTable v-else :data="data" class="flex-1" />
  </UContainer>
</template>
