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
  <div class="index">
    <div class="row">
      <div class="container">
        <!-- 左側選單 -->
        <div class="col-3">
          <ul class="nav flex-column">
            <li class="nav-item">
              <a class="nav-link navbar-brand" href="#">
                <img src="../assets/images/logo.svg" alt="">
              </a>
            </li>
            <li class="nav-item">
              <a class="nav-link active" aria-current="page" href="#">Dashboard</a>
            </li>
            <li class="nav-item">
              <a class="nav-link" href="#">Question</a>
            </li>
            <li class="nav-item">
              <a class="nav-link" href="#">Assignment</a>
            </li>
            <li class="nav-item">
              <a class="nav-link" href="#">Course</a>
            </li>
            <li class="nav-item">
              <a class="nav-link" href="#">Admin</a>
            </li>
            <li class="nav-item">
              <a class="nav-link" href="#">Settings</a>
            </li>
          </ul>
        </div>

        <!-- 右側內容 -->
        <div class="col-9">
          <div class="content">

          </div>
        </div>
      </div>
    </div>

  </div>

</template>