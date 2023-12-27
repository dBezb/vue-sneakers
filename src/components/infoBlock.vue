<script setup>
defineProps({
  title: String,
  description: String,
  imageUrl: String
})
</script>

<template>
  <div class="flex flex-col items-center">
    <img height="90" width="90" :src="imageUrl" alt="Info img" />
    <h2 class="mt-4 text-2xl font-medium">{{ title }}</h2>
    <p class="text-slate-500">{{ description }}</p>
  </div>
</template>
