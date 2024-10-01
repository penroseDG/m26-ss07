<template>
    <div>
      <h1>User List</h1>
  
      <!-- Nút mở form -->
      <button @click="toggleForm">Add user</button>
  
      <!-- Danh sách người dùng -->
      <ul>
        <li v-for="user in users" :key="user.email">
          {{ user.name }} - {{ user.email }} - {{ user.address }}
        </li>
      </ul>
  
      <!-- Gọi FormAddUser component -->
      <FormAddUser 
        :isVisible="showForm" 
        @close-form="toggleForm" 
        @add-user="addUser" 
      />
    </div>
</template>
  
<script>
  import FormAddUser from './FormAddUser.vue';
  
  export default {
    name: "ListUser",
    components: {
      FormAddUser
    },
    data() {
      return {
        users: [],
        showForm: false
      };
    },
    methods: {
      toggleForm() {
        this.showForm = !this.showForm;
      },
      addUser(user) {
        this.users.push(user);
      }
    }
  };
</script>
  
<style scoped>
  ul {
    list-style-type: none;
    padding: 0;
  }
  
  li {
    padding: 10px 0;
  }
</style>