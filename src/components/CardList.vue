<script setup>
import Card from './Card.vue'

const onClickAdd = () => {
  alert(11)
}
</script>
<template>
  <div class="grid grid-cols-4 gap-5">
    <Card
      title="Nike Blazer Mid Suede"
      :price="79"
      image-url="/sneakers/sneakers-1.jpg"
      :is-added="false"
      :is-favorite="false"
      :onClickAdd="onClickAdd"
    />
    <Card image-url="/sneakers/sneakers-2.jpg" />
    <Card />
    <Card />
    <Card />
    <Card />
  </div>
</template>
