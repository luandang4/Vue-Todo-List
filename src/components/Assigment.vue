<template>
  <li 
    :class="{
      'list-group-item px-3 py-1 d-flex align-items-center flex-grow-1 border-0 bg-transparent': true,
      'line-through': assigment.completed
    }"
  >
    <input class="form-check-input me-2" type="checkbox" value="" id="flexCheckChecked1" aria-label="..." v-model="assigment.completed"/>
    <p class="lead fw-normal mb-0">{{ assigment.name }}</p>
    <div class="d-flex flex-row justify-content-end ms-3">
      <a href="" class="text-danger" data-mdb-toggle="tooltip" title="Delete todo">
        <i class="fas fa-trash-alt"></i>
      </a>
    </div>
  </li>
</template>
<script setup>
  const props = defineProps({
    assigment: Object
  });
</script>


<style scoped>
.line-through {
  text-decoration: line-through;
}
</style>