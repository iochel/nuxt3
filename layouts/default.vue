<template>
    <div>
        
      <header class="shadow-sm bg-white">
        <nav class="container mx-auto p-1 absolute justify-between">
          <NuxtLink to="/" class="font-bold">iosoyvale</NuxtLink>
          <ul class="flex gap-7">
            <li><NuxtLink to="/">Home</NuxtLink></li>
            <li><NuxtLink to="/products" class="">Product</NuxtLink></li>
           
          </ul>
        </nav>
      </header>
      <div class="container mx-auto p-10">
        <slot />
      </div>
    </div>
  </template>
  
  <style scoped>
    .router-link-exact-active {
      color: #12b488;
    }
  
    .gap-7 {
      font-size: 23px;
    }
  </style>
  
  <script>
  useHead({
      title: 'Iosoyvale',
      meta: [
        { name: 'description', content: 'NuxtMerch'}
      ]
    })
  </script>