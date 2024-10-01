<template>
    <div class="card">
      <div class="card-header">
        <slot name="header"></slot>
      </div>
  
      <div class="card-body">
        <slot name="body"></slot>
      </div>
  
      <div class="card-footer">
        <slot name="footer"></slot>
      </div>
    </div>
</template>
  
<script>
  export default {
    name: "Card"
  };
</script>
  
  <style scoped>
  .card {
    border: 1px solid #ddd;
    border-radius: 8px;
    padding: 16px;
    box-shadow: 0 2px 8px rgba(0, 0, 0, 0.1);
    margin-bottom: 20px;
  }
  
  .card-header {
    font-size: 1.25rem;
    font-weight: bold;
    margin-bottom: 8px;
  }
  
  .card-body {
    font-size: 1rem;
    margin-bottom: 16px;
  }
  
  .card-footer {
    text-align: right;
  }
</style>