<template>
    <div>
      <h2>Count Children</h2>
      <!-- Nút Increment để phát sự kiện lên component cha -->
      <button @click="incrementCount">Increment</button>
    </div>
</template>
  
<script>
  export default {
    name: 'CountChildren',
    methods: {
      incrementCount() {
        // Phát sự kiện increment lên component cha
        this.$emit('increment');
      }
    }
  };
</script>