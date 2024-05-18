<script setup>
import Card from '@/components/Card.vue'

defineProps({
  items: Array,
  isSortedBy: Function,
  isSearchParams: Function
})
</script>

<template>
  <div class="flex flex-wrap gap-4 justify-center md:justify-between items-center pt-10 mx-10">
    <h2 class="text-3xl font-bold">Все кроссовки</h2>
    <div class="flex gap-5 items-center">
      <span>Сортировать</span>
      <select @change="isSortedBy" class="border rounded-2xl py-3 px-7">
        <option value="name">По названию</option>
        <option value="price">По цене (дешевые)</option>
        <option value="-price">По цене (доорогие)</option>
      </select>
    </div>
    <div class="relative">
      <img src="/search.svg" alt="search icon" class="absolute top-3.5 left-3" />
      <input
        @input="isSearchParams"
        type="text"
        placeholder="Поиск..."
        class="border border-slate-300 pl-8 pr-5 py-2 rounded-2xl"
      />
    </div>
  </div>
  <div
    class="grid justify-items-center md:grid-cols-2 lg:grid-cols-3 xl:grid-cols-4 gap-5 p-10 justify-center"
  >
    <Card
    v-for="item in items"
    :key="item.id"
    :title="item.title"
    :price="item.price"
    :image="item.imageUrl"
    />

  </div>
</template>
