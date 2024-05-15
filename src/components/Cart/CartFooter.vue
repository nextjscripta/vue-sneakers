<script setup></script>
<!--Верстка подвала в корзине-->
<template>
  <div class="flex flex-col mt-20 gap-5">
    <div class="flex justify-between">
      <span>Итого:</span>
      <div class="flex-1 border-b border-slate-300 mx-2"></div>
      <b>21 498 руб.</b>
    </div>
    <div class="flex justify-between">
      <span>Налог 5%:</span>
      <div class="flex-1 border-b border-slate-300 mx-2"></div>
      <b>1074 руб.</b>
    </div>

    <div class="bg-green-400 flex rounded-3xl p-3 justify-center relative cursor-pointer mt-6 hover:-translate-y-0.5 transition">
      <span class="text-white">Оформить заказ</span>
      <img src="/arrow-next.svg" alt="arrow next" class="absolute right-5 top-4" />
    </div>
  </div>
</template>

<style scoped></style>
