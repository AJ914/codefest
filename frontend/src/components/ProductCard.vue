<template>
    <div class="bg-white shadow-md p-4 rounded">
      <img :src="product.image" class="w-full h-40 object-cover" />
      <h3 class="text-lg font-bold mt-2">{{ product.name }}</h3>
      <p class="text-gray-600">{{ product.description }}</p>
      <p class="text-green-500 font-bold">${{ product.price }}</p>
    </div>
  </template>
  
  <script>
  export default {
    props: ['product']
  };
  </script>
  