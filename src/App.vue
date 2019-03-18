<template>
  <div id="app">
    <div 
      v-for="(product, index) in config"
      :key="index">
      <ProductCard
        :productName="product.name"
        :productCategory="product.categoryID"
      />
    </div>
  </div>
</template>

<script>
import mockConfig from './mock.js';
import ProductCard from './components/ProductCard.vue';

export default {
  name: 'app',
  components: {
    ProductCard
  },
  data() { 
    return {
      config: mockConfig.products,
    };
  },
}
</script>
