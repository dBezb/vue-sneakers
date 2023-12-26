<script setup>
import DrawerHeader from './DrawerHeader.vue'
import CartListItem from './CartListItem.vue'
</script>

<template>
  <div class="fixed top-0 left-0 h-full w-full bg-black z-10 opacity-80"></div>
  <div class="bg-white w-96 h-full fixed right-0 top-0 z-20 p-8">
    <DrawerHeader />
    <CartListItem />

    <div class="flex flex-col gap-5 my-6">
      <div class="flex gap-2">
        <span>Total:</span>
        <div class="flex-1 border-b border-dashed"></div>
        <b>140$</b>
      </div>
      <div class="flex gap-2">
        <span>Tax 5%:</span>
        <div class="flex-1 border-b border-dashed"></div>
        <b>7$</b>
      </div>

      <button
        disabled=""
        class="mt-2 transition bg-lime-500 w-full rounded-xl py-3 disabled:bg-slate-400 text-white hover:bg-lime-600 active:bg-lime-700 cursor-pointer"
      >
        Order up
      </button>
    </div>
  </div>
</template>
