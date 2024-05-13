<script setup>
import Header from '@/components/Header.vue'
import CardList from '@/components/CardList.vue'
import Drawer from '@/components/Drawer.vue'

</script>

<template>
  <Drawer/>
  <div class="w-4/5 m-auto bg-white rounded-xl mt-14 shadow-xl">
    <Header/>
    <CardList/>

  </div>
</template>
