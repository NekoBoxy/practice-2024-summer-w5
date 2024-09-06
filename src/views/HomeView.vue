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
    <div class="container">
      <div class="row">
        <!-- 左側選單 -->
        <div class="col-3">
          <a class="navbar-brand" href="#">
            <img src="../assets/images/logo.svg" alt="">
          </a>

          <ul class="nav flex-column">
            <li class="nav-item">
              <a class="nav-link active" aria-current="page" href="#">
                <span class="material-icons">assessment</span>
                <span class="nav-title">Dashboard</span>
              </a>
            </li>
            <li class="nav-item">
              <a class="nav-link" href="#">
                <span class="material-icons">question_answer</span>
                <div class="nav-title">Question</div>
              </a>
            </li>
            <li class="nav-item">
              <a class="nav-link" href="#">
                <span class="material-icons">assignment</span>
                <div class="nav-title">Assignment</div>
              </a>
            </li>
            <li class="nav-item">
              <a class="nav-link" href="#">
                <span class="material-icons">video_library</span>
                <div class="nav-title">Course</div>
              </a>
            </li>
            <li class="nav-item">
              <a class="nav-link" href="#">
                <span class="material-icons">people</span>
                <div class="nav-title">Admin</div>
              </a>
            </li>
            <li class="nav-item">
              <a class="nav-link" href="#">
                <span class="material-icons">settings</span>
                <div class="nav-title">Settings</div>
              </a>
            </li>
            <!-- 底部登入者頭像 -->
            <li class="nav-item">
              <a class="nav-link" href="#">
                <div class="d-flex justify-content-center">
                  <div class="avatar">
                    <img src="../assets/images/andychen.jpeg" alt="" srcset="">
                  </div>
                  <div class="data-box">
                    <p>Andy Chen</p>
                    <p>andy0401@mail.com</p>
                  </div>
                </div>
              </a>
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