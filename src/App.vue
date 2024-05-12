<script setup>
import MyHello from '@/components/MyHello.vue'
import Product from '@/components/Product.vue'
</script>

<template>

<!--  <MyHello/>-->

  <Product title="Nike" description="New design" :price='200'/>
  <Product />
  <Product/>
</template>

<style scoped>

</style>
