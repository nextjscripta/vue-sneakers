"id": 1
<script setup>
import Header from '@/components/Header.vue'
import CardList from '@/components/CardList.vue'
import Drawer from '@/components/Cart/Drawer.vue'
import { onMounted, ref, watch } from 'vue'
import axios from 'axios'

const items = ref([])
const sortBy = ref('')

onMounted(async ()=>{
    try {
      const {data} = await axios.get('https://443bfca0a207c10b.mokky.dev/products')
      items.value = data
    }
    catch (e) {
      console.log(e)
    }
})
watch(sortBy, async () => {
  try {
    const {data} = await axios.get(`https://443bfca0a207c10b.mokky.dev/products?sortBy=${sortBy.value}`)
    items.value = data
  }
  catch (e) {
    console.log(e)
  }
})
const isSortedBy = (event) => {
  sortBy.value = event.target.value
}


</script>

<template>
<!--  <Drawer/>-->
  <div class="w-11/12 lg:w-3/4 m-auto bg-white rounded-xl mt-14 shadow-xl">
    <Header/>
    <CardList :items="items" :isSortedBy="isSortedBy"/>
  </div>
</template>
