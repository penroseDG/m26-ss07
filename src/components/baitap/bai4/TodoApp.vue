<template>
    <div>
      <h1>Todo List</h1>
      <ul>
        <!-- Lặp qua danh sách todos và truyền từng todo xuống component con -->
        <li v-for="todo in todos" :key="todo.id">
          <TodoItem :todo="todo" @deleteTodo="handleDeleteTodo" />
        </li>
      </ul>
    </div>
</template>
  
<script>
  import TodoItem from './TodoItem.vue';
  
  export default {
    name: 'TodoApp',
    components: {
      TodoItem
    },
    data() {
      return {
        todos: [
          { id: 1, title: 'Learn Vue.js' },
          { id: 2, title: 'Build a Todo App' },
          { id: 3, title: 'Read Vue Documentation' }
        ]
      };
    },
    methods: {
      // Xử lý sự kiện xóa công việc khi nhận ID từ component con
      handleDeleteTodo(id) {
        this.todos = this.todos.filter(todo => todo.id !== id);
        console.log(`Deleted todo with id: ${id}`);
      }
    }
  };
</script>