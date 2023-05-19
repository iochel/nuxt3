<template>
    <div>
      <div class="grid grid-cols-3 gap-5">
        <div v-for="p in products">
          <ProductCard :product="p" />
        </div>
      </div>
    </div>
  </template>
  
  <script setup>
    //  fetch the products
    const { data: products } = await useFetch('https://fakestoreapi.com/products')
  
    definePageMeta({
      layout: "products",
    })
  
    useHead({
      title: 'Iosoyvale | Products',
      meta: [
        { name: 'description', content: 'NuxtMerch'}
      ]
    })
  </script>
  <style scoped>
      h2 {
          margin-bottom: 20px;
          font-size: 36px;
      }
  
      p {
          margin: 20px 0;
      }
  </style>