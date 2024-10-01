<template>
    <div class="modal-mask" v-if="isOpen">
      <div class="modal-wrapper">
        <div class="modal-container">
          <div class="modal-header">
            <slot name="header">
              <!-- Default tiêu đề nếu không có slot -->
              <h3>Modal Title</h3>
            </slot>
            <button class="close" @click="closeModal">×</button>
          </div>
  
          <div class="modal-body">
            <slot name="body">
              <!-- Default nội dung nếu không có slot -->
              <p>Modal Content</p>
            </slot>
          </div>
  
          <div class="modal-footer">
            <button @click="closeModal">Close</button>
          </div>
        </div>
      </div>
    </div>
</template>
  
<script>
  export default {
    props: {
      isOpen: {
        type: Boolean,
        default: false
      }
    },
    methods: {
      closeModal() {
        this.$emit('close');
      }
    }
  };
</script>
  
<style scoped>
  .modal-mask {
    position: fixed;
    z-index: 9998;
    top: 0;
    left: 0;
    width: 100%;
    height: 100%;
    background-color: rgba(0, 0, 0, 0.5);
    display: flex;
    justify-content: center;
    align-items: center;
  }
  
  .modal-wrapper {
    display: flex;
    justify-content: center;
    align-items: center;
    width: 100%;
  }
  
  .modal-container {
    background-color: white;
    width: 300px;
    padding: 20px;
    border-radius: 5px;
  }
  
  .modal-header {
    display: flex;
    justify-content: space-between;
    align-items: center;
  }
  
  .close {
    background: none;
    border: none;
    font-size: 1.5rem;
    cursor: pointer;
  }
  
  .modal-footer {
    display: flex;
    justify-content: flex-end;
  }
</style>
  