<script>
export default {
  data() {
    return {
      name: 'default_name',
      category: 'default_category',
    }
  },
  methods: {
    addToCart(msg) {
      // here is logic for core functionality of product components
      alert( msg + ' is now in your cart')
    }
  }
}
</script>