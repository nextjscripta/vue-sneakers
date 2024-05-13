<script setup>
defineProps({
  title: String,
  price: Number,
  image: String,
  isAdded: Boolean,
  isFavorite: Boolean,
  isFavoriteClicked: Function,
  isAddClicked: Function
})

</script>

<template>
  <div
    class="relative p-7 shadow-xl border border-slate-300 max-w-60 rounded-3xl transition hover:-translate-y-1 transform-gpu"
  >
    <img
      :src="isFavorite ? 'like-2.svg' : 'like-1.svg'"
      alt="like"
      class="absolute top-8 left-8 cursor-pointer shadow-xl"
      @click="isFavoriteClicked"
    />
    <img :src="image" alt="" class="w-48" />
    <h2 class="text-sm mt-5">{{ title }}</h2>
    <div class="flex justify-between items-center mt-3.5">
      <div>
        <span class="text-xs uppercase text-slate-400">Цена</span>
        <p class="text-sm font-bold">{{ price }} руб.</p>
      </div>
      <div>
        <img
          :src="isAdded ? '/checked.svg' : '/plus.svg'"
          alt="Кнопка плюс"
          class="cursor-pointer shadow-xl"
        />
      </div>
    </div>
  </div>
</template>
