<script setup>
import Learning from './components/Learning.vue'
import ToDo from './components/ToDo.vue'
import Assignment from './components/Assigment.vue'
</script>

<template>
  <main>
    <section>
      <div class="row">
        <div class="col"><ToDo/></div>
        <div class="col"><Learning/></div>
      </div>
      <div class="row">
        <div class="col"><Assignment/></div>
        <div class="col"></div>
      </div>
    </section>
  </main>
</template>

<style scoped>

</style>
