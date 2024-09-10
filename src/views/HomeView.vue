<script setup>
import { ref, onMounted } from "vue";
// import CModal from "@/components/CModal.vue";

const verifyToCht = function (state) {
  let cht = "";

  if (state) {
    cht = "Yes";
  } else {
    cht = "No";
  }

  return cht;
}

const tableData = ref(
  [
    {
      id: 1,
      name: "Emir Wicks",
      email: "emir.wicks@mail.com",
      verified: true,
      isVisible: true
    },
    {
      id: 2,
      name: "Zaina Goldsmith",
      email: "zaina.goldsmith@mail.com",
      verified: true,
      isVisible: true
    },
    {
      id: 3,
      name: "Mahima Lopez",
      email: "mahima.lopez@mail.com",
      verified: true,
      isVisible: true
    },
    {
      id: 4,
      name: "Pharrell Murray",
      email: "pharrell.murray@mail.com",
      verified: true,
      isVisible: true
    },
    {
      id: 5,
      name: "Annika Mcbride",
      email: "annika.mcbride@mail.com",
      verified: true,
      isVisible: true
    },
    {
      id: 6,
      name: "Fatimah Clark",
      email: "fatimah.clark@mail.com",
      verified: true,
      isVisible: true
    },
    {
      id: 7,
      name: "Klaudia Rhodes",
      email: "klaudia.rhodes@mail.com",
      verified: true,
      isVisible: true
    },
    {
      id: 8,
      name: "Tillie Lucero",
      email: "tillie.lucero@mail.com",
      verified: true,
      isVisible: true
    },
    {
      id: 9,
      name: "Sabrina Stephenson",
      email: "sabrina.stephenson@mail.com",
      verified: true,
      isVisible: true
    },
    {
      id: 10,
      name: "Annie Smith",
      email: "annie.smith@mail.com",
      verified: true,
      isVisible: true
    },
  ]
);

const submitEdit = function (data) {
  console.log("data: ", data);
};

onMounted(() => {

});
</script>

<template>
  <div class="container">
    <div class="row">
      <!-- 左側選單 -->
      <div class="col-3 aside-menu position-relative d-flex flex-column">
        <div class="top-group">
          <a class="navbar-brand" href="javascript:;">
            <img src="../assets/images/logo.svg" alt="">
          </a>

          <ul class="nav flex-column">
            <li class="nav-item">
              <a class="nav-link active" aria-current="page" href="javascript:;">
                <span class="material-icons">assessment</span>
                <span class="nav-title">Dashboard</span>
              </a>
            </li>
            <li class="nav-item">
              <a class="nav-link" href="javascript:;">
                <span class="material-icons">question_answer</span>
                <div class="nav-title">Question</div>
              </a>
            </li>
            <li class="nav-item">
              <a class="nav-link" href="javascript:;">
                <span class="material-icons">assignment</span>
                <div class="nav-title">Assignment</div>
              </a>
            </li>
            <li class="nav-item">
              <a class="nav-link" href="javascript:;">
                <span class="material-icons">video_library</span>
                <div class="nav-title">Course</div>
              </a>
            </li>
            <li class="nav-item">
              <a class="nav-link" href="javascript:;">
                <span class="material-icons">people</span>
                <div class="nav-title">Admin</div>
              </a>
            </li>
            <li class="nav-item">
              <a class="nav-link" href="javascript:;">
                <span class="material-icons">settings</span>
                <div class="nav-title">Settings</div>
              </a>
            </li>
          </ul>
        </div>

        <!-- 底部登入者頭像 -->
        <div class="user position-absolute">
          <a href="javascript:;">
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
        </div>
      </div>

      <!-- 右側內容 -->
      <div class="col-9 main-table position-relative">
        <div class="table-ctrl d-flex justify-content-between align-items-center">
          <div class="group-start d-flex">
            <span class="admin">Admin</span>

            <button type="button" class="btn btn-add">
              <span class="material-icons">add</span>
              <span>Add New Admin</span>
            </button>
          </div>

          <div class="group-end">
            <button type="button" class="btn btn-search">
              <span class="material-icons">search</span>
            </button>

            <button type="button" class="btn btn-notify">
              <span class="material-icons">notifications_active</span>
            </button>
          </div>
        </div>

        <table class="table-content table table-striped">
          <thead>
            <tr>
              <th scope="col" class="table-title">ID
                <a href="javascript:;">
                  <span class="material-icons">arrow_downward</span>
                </a>
              </th>
              <th scope="col" class="table-title">Name</th>
              <th scope="col" class="table-title">Email</th>
              <th scope="col" class="table-title">Verified</th>
              <th scope="col" class="table-title"></th>
            </tr>
          </thead>

          <tbody>
            <tr v-for="item in tableData" :key="item.id">
              <td scope="row" class="table-row-id">#{{ item.id }}</td>
              <td>{{ item.name }}</td>
              <td>{{ item.email }}</td>
              <td>{{ verifyToCht(item.verified) }}</td>
              <td class="table-row-ctrl">
                <span class="material-icons icon-visible" v-if="item.isVisible">visibility</span>
                <span class="material-icons icon-visible" v-else>visibility_off</span>
                <span class="material-icons icon-edit">edit</span>

                <!-- <CModal :data="item" :is-modal-show="item.isVisible" @click="submitEdit(result)">
                    <span class="material-icons icon-edit">edit</span>
                  </CModal> -->
              </td>
            </tr>
          </tbody>
        </table>

        <nav aria-label="pagination">
          <ul class="pagination justify-content-end align-items-stretch">
            <li class="page-item disabled">
              <a class="page-link" aria-label="Previous">
                <span class="material-icons">chevron_left</span>
              </a>
            </li>

            <li class="page-item page-num-style active">
              <a class="page-link" aria-current="page">1</a>
            </li>

            <li class="page-item page-num-style">
              <a class="page-link" href="javascript:;">2</a>
            </li>

            <li class="page-item page-num-style">
              <a class="page-link" href="javascript:;">3</a>
            </li>

            <li class="page-item">
              <a class="page-link" href="javascript:;" aria-label="Next">
                <span class="material-icons">chevron_right</span>
              </a>
            </li>
          </ul>
        </nav>

        <!-- ori -->
        <!-- <div class="pagination d-flex flex-row justify-content-end align-items-center">
          <div class="page-item mui-icon">
            <a href="javascript:;">
              <span class="material-icons">chevron_left</span>
            </a>
          </div>
          <div class="page-item page-border page-active">
            <a href="javascript:;">
              1
            </a>
          </div>
          <div class="page-item page-border">
            <a href="javascript:;">
              2
            </a>
          </div>
          <div class="page-item page-border">
            <a href="javascript:;">
              3
            </a>
          </div>
          <div class="page-item mui-icon">
            <a href="javascript:;">
              <span class="material-icons">chevron_right</span>
            </a>
          </div>
        </div> -->
      </div>
    </div>
  </div>

</template>