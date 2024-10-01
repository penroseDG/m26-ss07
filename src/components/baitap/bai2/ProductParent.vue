<template>
    <div>
      <h1>Product Parent</h1>
      <!-- Truyền đối tượng product xuống ProductChildren -->
      <ProductChildren :product="product" />
    </div>
</template>
  
<script>
  import ProductChildren from './ProductChildren.vue';
  
  export default {
    name: 'ProductParent',
    components: {
      ProductChildren
    },
    data() {
      return {
        product: {
          id: 1,
          name: 'Bưởi Ba Roi',
          price: 12000,
          quantity: 10
        }
      };
    }
  };
</script>