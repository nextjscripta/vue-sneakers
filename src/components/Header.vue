<script setup></script>

<template>
  <div class="flex justify-between items-center border-b border-slate-300 py-11 px-8">
    <div class="flex items-center gap-4">
      <img src="/logo.png" alt="logo" class="w-10"/>
      <div class="hidden md:block ">
        <h2 class="font-bold text-xl uppercase">Vue Sneakers</h2>
        <p class="uppercase font-normal text-slate-400">Магазин лучших кроссовок</p>
      </div>
    </div>
    <ul class="flex gap-8">
      <li class="flex gap-3 text-slate-500 cursor-pointer hover:text-black">
        <img src="/cart.svg" alt="Логотип корзины" />
        <b class="font-normal text-sm">1205 руб.</b>
      </li>
      <li class="flex gap-3 text-slate-500 cursor-pointer hover:text-black">
        <img src="/heart.svg" alt="Логотип сердце" />
        <span class="font-normal text-sm">Закладки</span>
      </li>
      <li class="flex gap-3 text-slate-500 cursor-pointer hover:text-black">
        <img src="/cart.svg" alt="Логотип профиль" />
        <span class="font-normal text-sm ">Профиль</span>
      </li>
    </ul>
  </div>
</template>

<style scoped></style>
