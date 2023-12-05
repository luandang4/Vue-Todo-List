<script setup>
import { ref, onMounted } from 'vue'
import BaseSection from './BaseSection.vue'

const count = ref(0)
const attributes = ref({
  elmClass: '',
  active: true,
  text: `Color of button changed!`
})

function increment() {
  count.value++
}

function alertToggle() {
  alert(attributes.value.text)
}

function setClassName() {
  attributes.value.active ? attributes.value.elmClass = 'btn btn-success' : attributes.value.elmClass = 'btn btn-danger'
}

function changeClassName() {
  attributes.value.active = ! attributes.value.active
  setClassName()
  alertToggle()
}

onMounted(() => {
  setClassName()
  console.log(`The initial count is ${count.value}`)
})

</script>
<template>
  <BaseSection>
    <h1>Learning</h1>

    <input type="number" class="form-control form-control-lg" v-model="count">
    <p>Count value: {{ count }}</p>
    <button type="button" class="btn btn-primary me-2" @click="increment">Count++</button>
    <button type="button" :class="attributes.elmClass" @click="changeClassName">Click me</button>
  </BaseSection>
</template>

<style scoped>

</style>