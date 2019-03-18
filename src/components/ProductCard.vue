<template>
    <div :data-category="this.productCategory">
      <p>{{this.productName}}</p>
      <button v-on:click="addTo()">Add to cart</button>
    </div>
</template> 

<script>
import Product from '../core/Product.vue';

export default { 
  name: 'ProductCard',
  extends: Product,
  props: {
    productCategory: {
      type: String,
      default: ''
    },
    productName: {
      type: String,
      default: ''
    },
  },
  methods: {
    // Here I can extend function from core component - Product
    addTo() {
      this.addToCart(this.productName)
      // other logic if needed
    }
  },
  mixins: [Product]
}
</script>

<style scoped>
</style>
