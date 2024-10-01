<template>
    <div v-if="isVisible" class="form-container">
      <h2>Add New User</h2>
      <form @submit.prevent="submitForm">
        <div>
          <label for="name">Name:</label>
          <input type="text" id="name" v-model="name" required />
        </div>
        <div>
          <label for="email">Email:</label>
          <input type="email" id="email" v-model="email" required />
        </div>
        <div>
          <label for="address">Address:</label>
          <input type="text" id="address" v-model="address" required />
        </div>
        <button type="button" @click="closeForm">Close</button>
        <button type="submit">Submit</button>
      </form>
    </div>
</template>
  
<script>
  export default {
    name: "FormAddUser",
    props: {
      isVisible: {
        type: Boolean,
        required: true
      }
    },
    data() {
      return {
        name: "",
        email: "",
        address: ""
      };
    },
    methods: {
      closeForm() {
        this.$emit('close-form');
      },
      submitForm() {
        const newUser = {
          name: this.name,
          email: this.email,
          address: this.address
        };
        this.$emit('add-user', newUser);
        this.name = "";
        this.email = "";
        this.address = "";
        this.closeForm();
      }
    }
  };
</script>
  
<style scoped>
  .form-container {
    border: 1px solid #ccc;
    padding: 20px;
    margin: 20px 0;
  }
</style>