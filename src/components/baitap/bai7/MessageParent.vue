<template>
    <div>
      <h2>Message from the child component:</h2>
      <p v-if="message">{{ message }}</p>
  
      <!-- Include the child component -->
      <MessageChildren @message-sent="handleMessage" />
    </div>
</template>
  
<script>
  import MessageChildren from './MessageChildren.vue';
  
  export default {
    name: "MessageParent",
    components: {
      MessageChildren
    },
    data() {
      return {
        message: null
      };
    },
    methods: {
      handleMessage(msg) {
        this.message = msg;
      }
    }
  };
</script>