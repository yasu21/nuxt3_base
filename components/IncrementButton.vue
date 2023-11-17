<template>
  <VBtn @click="increment">{{ counter }}</VBtn>
</template>
<script setup lang="ts">
const counter = ref(0)
const increment = () => {
  counter.value++
}
</script>
