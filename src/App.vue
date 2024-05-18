<script setup>
import Header from '@/components/Header.vue'
import CardList from '@/components/CardList.vue'
import Drawer from '@/components/Cart/Drawer.vue'
import { onMounted, reactive, ref, watch } from 'vue'
import axios from 'axios'

const items = ref([])
const sortRef = reactive({
  sortBy: 'title',
  searchParams: ''
})

const fetchData = async () => {
  try {
    const params = {
      sortBy: sortRef.sortBy
    }
    if (sortRef.searchParams) {
        params.title = `*${sortRef.searchParams}*`
    }


    const {data} = await axios.get('https://443bfca0a207c10b.mokky.dev/products', {
      params
    })
    items.value = data
  }
  catch (e) {
    console.log(e)
  }
}

onMounted(async ()=>{
  await fetchData()
})
watch(sortRef, fetchData)

const isSortedBy = (event) => {
  sortRef.sortBy = event.target.value
}

const isSearchParams = (e) => {
  sortRef.searchParams = e.target.value
}


</script>

<template>
<!--  <Drawer/>-->
  <div class="w-11/12 lg:w-3/4 m-auto bg-white rounded-xl mt-14 shadow-xl">
    <Header/>
    <CardList :items="items" :isSortedBy="isSortedBy" :isSearchParams="isSearchParams"/>
  </div>
</template>
