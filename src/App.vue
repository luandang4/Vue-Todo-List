<script setup>
import Learning from './components/Learning.vue'
import ToDo from './components/ToDo.vue'
import Assignments from './components/Assigments.vue'
import LearnProp from './components/LearnProp.vue';
</script>

<template>
  <main>
    <section>
      <div class="row">
        <div class="col"><ToDo/></div>
        <div class="col"><Learning/></div>
      </div>
      <div class="row">
        <div class="col"><Assignments/></div>
        <div class="col"><LearnProp/></div>
      </div>
    </section>
  </main>
</template>

<style scoped>

</style>
