<template>
    <div>
      <h1>Parent Component</h1>
      <!-- Truyền biến companyName xuống ChildrenComponent thông qua prop -->
      <ChildrenComponent :company-name="companyName" />
    </div>
</template>
  
<script>
  import ChildrenComponent from './ChildrenComponent.vue';
  
  export default {
    name: 'ParentComponent',
    components: {
      ChildrenComponent
    },
    data() {
      return {
        companyName: 'Rikkei Academy' // Biến đại diện cho tên công ty
      };
    }
  };
</script>