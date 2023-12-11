<template>
  <form @submit.prevent="add">
    <div class="d-flex flex-row align-items-center">
      <input v-model="newAssigment" type="text" class="form-control form-control-lg" id="exampleFormControlInput1" placeholder="Add new...">
      <button type="submit" class="btn btn-primary mx-2 py-2">Add</button>
    </div>
  </form>
</template>

<script setup>
import { ref, defineEmits } from 'vue';

const newAssigment = ref('');
const emit = defineEmits();

function add() {
  console.log(12123);

  emit("add", newAssigment);

  newAssigment.value = '';
}

</script>