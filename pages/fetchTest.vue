<template>
  <VContainer>
    <div>fetchTest</div>
    <div v-if="error">{{ error }}</div>
    <div v-else-if="pending">
      <v-skeleton-loader type="article"></v-skeleton-loader>
    </div>
    <div v-else>
      <li v-for="(item, i) in data as any" :key="i">
        {{ item.title }}
      </li>
    </div>
    <v-btn @click="refresh">refresh</v-btn>
    <v-btn to="/">home</v-btn>
  </VContainer>
</template>
<script setup lang="ts">
const { data, pending, error, refresh } = await useAsyncData('mountains', () =>
  $fetch('https://api.nuxtjs.dev/mountains')
)
</script>
