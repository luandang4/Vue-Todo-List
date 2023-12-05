<script setup>
import { ref, computed, onMounted } from 'vue'
import BaseSection from './BaseSection.vue'

const assigments = ref([
  { id: 1, name: 'Write rspec No.1', completed: false },
  { id: 2, name: 'Write rspec No.2', completed: false },
  { id: 3, name: 'Write rspec No.3', completed: false },
  { id: 4, name: 'Write rspec No.4', completed: false },
])

const inProgressAssignment = computed(() => {
  return assigments.value.filter(assigment => !assigment.completed)
})

const completedAssignment = computed(() => {
  return assigments.value.filter(assigment => assigment.completed)
})

</script>
<template>
  <BaseSection>
    <div v-if="inProgressAssignment.length">
      <p class="h3 mt-3 mb-4 pb-3 text-primary">In Progress</p>
      <ul>
        <li class="list-group-item px-3 py-1 d-flex align-items-center flex-grow-1 border-0 bg-transparent"
          v-for="assigment in inProgressAssignment"
          :key="assigment.id"
        >
          <input class="form-check-input me-2" type="checkbox" value="" id="flexCheckChecked1" aria-label="..." v-model="assigment.completed"/>
          <p class="lead fw-normal mb-0">{{ assigment.name }}</p>
        </li>
      </ul>
    </div>

    <div v-if="completedAssignment.length">
      <p class="h3 mt-3 mb-4 pb-3 text-primary">Completed</p>
      <ul>
        <li class="list-group-item px-3 py-1 d-flex align-items-center flex-grow-1 border-0 bg-transparent"
          v-for="assigment in completedAssignment"
          :key="assigment.id"
        >
          <input class="form-check-input me-2" type="checkbox" value="" id="flexCheckChecked1" aria-label="..." v-model="assigment.completed"/>
          <p class="lead fw-normal mb-0">{{ assigment.name }}</p>
        </li>
      </ul>
    </div>
    <pre>{{ assigments }}</pre>
  </BaseSection>
</template>

<style scoped>

</style>