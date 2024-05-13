<script setup>
import Card from '@/components/Card.vue'


const isFavoriteClicked = () => {
  alert('clicked')
}

const isAddClicked = () => {
 alert('clicked')
}

</script>

<template>
  <div class="flex flex-wrap justify-between items-center pt-10 mx-10">
    <h2 class="text-3xl font-bold ">Все кроссовки</h2>
    <input type="text" placeholder="Поиск..." class="border border-slate-300 px-5 py-2 rounded-2xl">
  </div>
  <div class="grid sm:grid-cols-2 lg:grid-cols-3 xl:grid-cols-4 gap-5 p-10 justify-center">
    <Card title="Мужские Кроссовки" price="12 999" image="/sneakers/sneakers-2.jpg"/>
  </div>
</template>

<style scoped></style>
