<template>
  <div v-if="assigments.length">
    <p class="h3 mt-3 mb-4 pb-3 text-primary">{{ title }}</p>
    <ul>
      <Assigment
        v-for="assigment in assigments"
        :key="assigment.id"
        :assigment="assigment"
      ></Assigment>
    </ul>
  </div>
</template>

<script setup>
import Assigment from './Assigment.vue'

const props = defineProps({
  title: String,
  assigments: Array
});
</script>
