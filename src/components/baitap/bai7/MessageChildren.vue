<template>
    <div>
      <button @click="sendMessage">Send message</button>
    </div>
</template>
  
<script>
  export default {
    name: "MessageChildren",
    methods: {
      sendMessage() {
        this.$emit('message-sent', 'This is a message from the child component.');
      }
    }
  };
</script>