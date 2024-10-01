<template>
    <div>
      <h2>Dữ liệu trong component con</h2>
      <p><strong>Id:</strong> {{ product.id }}</p>
      <p><strong>Product name:</strong> {{ product.name }}</p>
      <p><strong>Price:</strong> {{ product.price.toLocaleString() }} đ</p>
      <p><strong>Quantity:</strong> {{ product.quantity }}</p>
      <i>Dữ liệu trong ProductChildren.vue</i>
    </div>
</template>
  
<script>
  export default {
    name: 'ProductChildren',
    props: {
      product: {
        type: Object,
        required: true
      }
    }
  };
</script>