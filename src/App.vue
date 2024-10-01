<template>
  <div>
    <h1>Home Page</h1>
    <p>_______________________________</p>
    <ParentComponent></ParentComponent>
    <ParentComponent></ParentComponent>
    <ProductParent></ProductParent>
    <CountParent></CountParent>
    <TodoApp></TodoApp>

    <BaseButton title="Click me"/>
    <BaseButton title="Add product"/>
    <SlotComponent>
      <a href="">Facebook</a>
    </SlotComponent>

    <BaseButton @click="handeClick">
      <a href="">Click me</a>
    </BaseButton>

    <h1>App Component</h1>
    <button @click="showModal = true">Show Modal</button>

    <!-- Modal component -->
    <Modal :isOpen="showModal" @close="showModal = false">
      <template v-slot:header>
        <h3>Thông báo từ hệ thống</h3>
      </template>

      <template v-slot:body>
        <p>Đây là nội dung của modal. Bạn có thể đóng modal bằng cách nhấn vào nút 'Close'.</p>
      </template>
    </Modal>

    <Card>
      <template v-slot:header>
        Thông tin sản phẩm
      </template>

      <template v-slot:body>
        Đây là mô tả ngắn gọn về sản phẩm này. Sản phẩm có các tính năng nổi bật và giá cả hợp lý.
      </template>

      <template v-slot:footer>
        <button @click="viewDetails">Xem chi tiết</button>
      </template>
    </Card>

    <MessageParent></MessageParent>
    <ListUser></ListUser>
  </div>
  
</template>

<script setup>
import ParentComponent from './components/ParentComponent.vue';
import BaseButton from './components/BaseButton.vue';
import SlotComponent from './components/SlotComponent.vue';
import ParentComponent from './components/baitap/bai1/ParentComponent.vue';
import ProductParent from './components/baitap/bai2/ProductParent.vue';
import CountParent from './components/baitap/bai3/CountParent.vue';
import TodoApp from './components/baitap/bai4/TodoApp.vue';
import Modal from './components/baitap/bai5/Modal.vue';
import Card from './components/baitap/bai6/Card.vue';
import MessageParent from './components/baitap/bai7/MessageParent.vue';
import ListUser from './components/baitap/bai8/ListUser.vue';

const handeClick = () => {
  console.log("Clicked");
};

const handleClickParent = (data) => {
  console.log("Dữ liệu truyền từ con: ", data)
};

</script>

<style></style>