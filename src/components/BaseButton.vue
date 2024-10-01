<template>
  <!-- Bước 2: Phát sự kiện thông qua emit -->
  <button @click="handleClick">
    <slot></slot>
  </button>
</template>

<script setup>
const props = defineProps({
    title: {
        default: "Click me 1",
        type: String,
        required: true,
    }
});

// Bước 1: Khởi tạo ra các emit
const emit = defineEmits(["onClick"]);
console.log("Props", props);

const handeClick = () => {
    emit("onClick", "Xin chào các bạn");
}
</script>

<style></style>