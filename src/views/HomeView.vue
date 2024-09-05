<script setup>
// import { ref, onMounted } from "vue";

// 法 1 - 只引入需要的功能
// import { Modal } from 'bootstrap';
// const myModal = ref(null);

// onMounted(() => {
//   const test = new Modal(myModal.value);
//   test.show();
// })

// 法 2 - 引入全部的 bootstrap
// import * as bootstrap from 'bootstrap';
// const myModal = ref(null);

// onMounted(() => {
//   const test = new bootstrap.Modal(myModal.value, {});
//   test.show();
// });

// 法 3 - 跟法 1 有點像，只是引入檔案的路徑更明確
// import * as bootstrap from 'bootstrap'; // 依需求決定是否引入全部
// import Modal from 'bootstrap/js/dist/modal';
// const myModal = ref(null);

// onMounted(() => {
//   const test = new Modal(myModal.value);
//   test.show();
// });
</script>

<template>
  <div class="nav">
    <div class="container">

    </div>
  </div>
  
  <div class="content">
    <div class="container">

    </div>
  </div>
</template>
