<template>
    <div>
      <h1>Count Parent</h1>
      <p>Current Count: {{ count }}</p>
      <!-- Truyền biến count và hàm updateCount cho CountChildren -->
      <CountChildren @increment="updateCount" />
    </div>
</template>
  
<script>
  import CountChildren from './CountChildren.vue';
  
  export default {
    name: 'CountParent',
    components: {
      CountChildren
    },
    data() {
      return {
        count: 0 // Giá trị khởi tạo cho count
      };
    },
    methods: {
      updateCount() {
        this.count += 1; // Tăng biến đếm mỗi khi nhận được sự kiện increment
      }
    }
  };
</script>