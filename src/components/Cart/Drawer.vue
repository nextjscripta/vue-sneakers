<script setup>
import CartItem from '@/components/Cart/CartItem.vue'
import CartList from '@/components/Cart/CartList.vue'
import CartFooter from '@/components/Cart/CartFooter.vue'
</script>

<template>
  <div class="fixed top-0 left-0 w-full h-full z-10 bg-black opacity-70"></div>
  <div class="fixed right-0 top-0 h-full w-1/4 z-20 bg-white">
    <div class="m-8 ">
      <h2 class="text-2xl font-bold">Корзина</h2>
      <div class="flex flex-col">
        <CartList />
        <CartFooter />
      </div>
    </div>
  </div>
</template>
