<template>
  <VContainer>
    {{ email }}
    <IncrementButton />
    <v-btn to="/fetchTest">test</v-btn>
  </VContainer>
</template>

<script setup>
// import IncrementButton from '@/components/IncrementButton.vue'

const email = ref('email')
</script>
