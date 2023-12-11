<template>
  <BaseSection>
    <AssigmentList :assigments="filters.inProgress" title="In Progress"></AssigmentList>
    <AssigmentList :assigments="filters.completed" title="Completed"></AssigmentList>
    <AssugmentCreate @add="handleAdd"></AssugmentCreate>
    <!-- <pre>{{ assigments }}</pre> -->
  </BaseSection>
</template>

<script setup>
import { ref, computed, onMounted } from 'vue'
import BaseSection from './BaseSection.vue'
import AssigmentList from './AssigmentList.vue'
import AssugmentCreate from './AssugmentCreate.vue';

const assigments = ref([
  { id: 1, name: 'Write rspec No.1', completed: false },
  { id: 2, name: 'Write rspec No.2', completed: false },
  { id: 3, name: 'Write rspec No.3', completed: false },
  { id: 4, name: 'Write rspec No.4', completed: false },
])

const filters = computed(() => {
  return {
    inProgress: assigments.value.filter(assigment => !assigment.completed),
    completed:  assigments.value.filter(assigment => assigment.completed)
  }
})

function handleAdd(name){
  assigments.value.push({
    id:        assigments.value.length + 1,
    name:      name.value,
    completed: false
  });
}
</script>
