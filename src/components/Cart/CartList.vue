<script setup>
import CartItem from '@/components/Cart/CartItem.vue'
</script>

<!--Верстка всех карточек в корзине-->
<template>
  <div class="mt-8 flex flex-col gap-2">
    <CartItem />
    <CartItem />
    <CartItem />
  </div>
</template>

<style scoped></style>
