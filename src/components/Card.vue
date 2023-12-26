<script setup>
defineProps({
  title: String,
  imageUrl: String,
  price: Number,
  isFavorite: Boolean,
  isAdded: Boolean,
  onClickAdd: Function,
  onClickFavorite: Function
})
</script>

<template>
  <div>
    <div
      class="bg-white relative border-slate-400 rounded-3xl p-8 cursor-pointer hover:translate-y-2 hover:shadow-xl"
    >
      <img
        :src="!isFavorite ? '/like-1.svg' : '/like-2.svg'"
        alt="Like 1"
        class="absolute top-8 left-8"
        @click="onClickFavorite"
      />
      <img :src="imageUrl" alt="Sneaker" />
      <p class="mt-2">{{ title }}</p>

      <div class="flex justify-between mt-2">
        <div class="flex flex-col">
          <span class="text-slate-400">Price:</span>
          <b>{{ price }}$</b>
        </div>

        <img @click="onClickAdd" :src="!isAdded ? '/plus.svg' : '/checked.svg'" alt="Plus" />
      </div>
    </div>
  </div>
</template>
