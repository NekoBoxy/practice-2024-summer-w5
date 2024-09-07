<script setup>
import { ref, onMounted } from "vue";

// 法 1 - 只引入需要的功能
// import { Modal } from 'bootstrap';

// const myModal = ref(null);
const props = defineProps({
  data: Object,
  isModalShow: Boolean
});




onMounted(() => {
  // const test = new Modal(myModal.value);
  // test.show();

  // console.log("props: ", props);
})
</script>

<template>
  <!-- <button type="button" class="btn btn-primary" data-bs-toggle="modal" data-bs-target="#exampleModal">
    <slot></slot>
  </button>

  <div class="modal fade" id="exampleModal" tabindex="-1" aria-labelledby="exampleModalLabel" aria-hidden="true"
    ref="myModal">
    <div class="modal-dialog">
      <div class="modal-content">
        <div class="modal-header">
          <h1 class="modal-title fs-5" id="exampleModalLabel">Modal title</h1>
          <button type="button" class="btn-close" data-bs-dismiss="modal" aria-label="Close"></button>
        </div>
        <div class="modal-body">
          嗨
        </div>
        <div class="modal-footer">
          <button type="button" class="btn btn-secondary" data-bs-dismiss="modal">Close</button>
          <button type="button" class="btn btn-primary">Save changes</button>
        </div>
      </div>
    </div>
  </div> -->
</template>

<style scoped></style>
