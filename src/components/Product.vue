<script setup>
 const props = defineProps({
  title: String,
   description: String,
   price: Number,
  })
 console.log(props)
</script>

<template>
<div class="product">
  <h2>{{title}}</h2>
  <h4>{{description}}</h4>
  <p>{{price}}</p>
</div>
</template>

<style scoped>
.product{
  border: 1px solid;
}
</style>