<script setup>
import { ref, onMounted } from 'vue'
import axios from 'axios'

const favorites = ref([])

onMounted(async () => {
  try {
    const { data } = await axios.get('https://17d2615b053556fd.mokky.dev/favorites')
    favorites.value = data
  } catch (error) {
    console.error(error)
  }
})
</script>

<template>
  <h1 class="text-3xl font-bold mb-10">Favorites</h1>
  <div class="grid grid-cols-3 gap-5">
    <div
      class="bg-white relative border-slate-400 rounded-3xl p-8 cursor-pointer hover:translate-y-2 hover:shadow-xl"
      v-for="item in favorites"
      :key="item.id"
    >
      <img :src="item.item.imageUrl" alt="Sneaker Image" />
      <h2>{{ item.item.title }}</h2>
      <p class="text-slate-400">Price: ${{ item.item.price }}</p>
    </div>
  </div>
</template>
