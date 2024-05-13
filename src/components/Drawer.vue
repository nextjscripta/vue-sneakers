<script setup>
import CartItem from '@/components/CartItem.vue'
</script>

<template>
  <div class="fixed top-0 left-0 w-full h-full z-10 bg-black opacity-70"></div>
  <div class="fixed right-0 top-0 h-full w-1/4 z-20 bg-white">
    <div class="m-8">
      <h2 class="text-2xl font-bold">Корзина</h2>
      <div class="mt-8 flex flex-col gap-2">
        <CartItem />
        <CartItem />
        <CartItem />
      </div>
      <div class="flex flex-col">
        <span>Итого:</span>
        <span>Налог 5%:</span>
        <div class="bg-green-400 flex rounded-3xl p-3 justify-center relative cursor-pointer mt-6">
          <span class="text-white">Оформить заказ</span>
          <img src="/arrow-next.svg" alt="arrow next" class="absolute right-5 top-4" >
        </div>
      </div>
    </div>
  </div>
</template>
