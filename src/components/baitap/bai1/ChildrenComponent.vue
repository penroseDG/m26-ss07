<template>
    <div>
      <h2>Children Component</h2>
      <p>Tên công ty: {{ companyName }}</p>
    </div>
</template>
  
<script>
  export default {
    name: 'ChildrenComponent',
    props: {
      companyName: {
        type: String,
        required: true
      }
    }
  };
</script>