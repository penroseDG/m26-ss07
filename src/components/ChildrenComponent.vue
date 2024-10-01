<template>
  <div>
    <h1>ChildrenComponent</h1>
    <!-- Bước 3: Lấy giá trị từ props và render dữ liệu -->
    <h3>UserName of ChildrenComponent: {{ props.userNameProps }}</h3>
    <h3>Age of ChildrenComponent: {{ props.ageProps }}</h3>
  </div>
</template>

<script setup>
// Bước 1: Định nghĩa props bên trong component con
const { userNameProps, ageProps, userInfoProps} = defineProps([
    "userNameProps",
    "ageProps",
    "userInfoProps",
]);

console.log("Props: ", props);
</script>

<style>

</style>