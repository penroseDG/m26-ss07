<template>
    <div>
      <span>{{ todo.title }}</span>
      <button @click="deleteTodo">Delete</button>
    </div>
</template>
  
<script>
  export default {
    name: 'TodoItem',
    props: {
      todo: {
        type: Object,
        required: true
      }
    },
    methods: {
      deleteTodo() {
        // Phát sự kiện deleteTodo và gửi ID của công việc lên component cha
        this.$emit('deleteTodo', this.todo.id);
      }
    }
  };
</script>
  
<style scoped>
  button {
    margin-left: 10px;
    color: red;
    cursor: pointer;
  }
</style>