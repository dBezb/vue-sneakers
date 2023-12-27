<script setup>
import { inject } from 'vue'
import CartItem from './CartItem.vue'

const { cart, removeFromCart } = inject('cart')
</script>

<template>
  <div class="flex flex-col flex-1 gap-2">
    <CartItem
      v-for="item in cart"
      :key="item.id"
      :item="item"
      :title="item.title"
      :price="item.price"
      :imageUrl="item.imageUrl"
      @on-click-remove="removeFromCart(item)"
    />
  </div>
</template>
