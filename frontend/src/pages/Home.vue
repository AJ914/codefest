<template>
    <div class="p-10">
      <h2 class="text-2xl font-bold">Latest Gadgets</h2>
      <div class="grid grid-cols-3 gap-4 mt-4">
        <ProductCard v-for="product in products" :key="product.id" :product="product" />
      </div>
    </div>
  </template>
  
  <script>
  import axios from 'axios';
  import ProductCard from '../components/ProductCard.vue';
  
  export default {
    components: {
      ProductCard
    },
    data() {
      return {
        products: []
      };
    },
    async created() {
      const response = await axios.get('http://127.0.0.1:8000/products');
      this.products = response.data;
    }
  };
  </script>
  