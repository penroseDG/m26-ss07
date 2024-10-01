<template>
    <div>
      <h1>Parent component</h1>
      <h3>UserName of ParentComponent: {{ userName }}</h3>
      <p>_______________________________</p>

      <!-- Sử dụng component con -->
      <!-- Bước 2: Trong component cha, gọi props được khai báo bên con và truyền giá trị cho nó -->
      <ChildrenComponent
        :userInfoProps="userInfo" 
        :userNameProps="userName" 
        :ageProps="age"
      />
    </div>
</template>

<script setup>
import ChildrenComponent from './ChildrenComponent.vue';

const userName = "Nguyen Van A";
// Tạo biến tuổi, truyền từ ParenComponent xuống ChildrenComponent
const age = 20;

const userInfo = {
    id: 1,
    name: "Nguyen Van B",
    age: 21,
};
</script>

<style>

</style>