<script setup>
import HelloWorld from './components/HelloWorld.vue'
import TheWelcome from './components/TheWelcome.vue'
import { ref, onMounted } from 'vue'

const count = ref(0)
const isButtonDisabled = ref(true)
const objectOfAttrs = {
  id: 'container',
  class: 'wrapper'
}
const eventName = 'href'

function getUrl() {
  return 'https://vuejs.org/guide/essentials/template-syntax.html'
}

function increment() {
  console.log(count.value);
  count.value++
}

function triggerError() {
  throw new Error('This is a test error!');
}

onMounted(() => {
  console.log(`The initial count is ${count.value}`)
})
</script>

<template>
  <header>
    <img alt="Vue logo" class="logo" src="./assets/logo.svg" width="125" height="125" />

    <div class="wrapper">
      <HelloWorld msg="My name is Dang Van Luan. I was doing it!" />
    </div>
  </header>

  <main>
    <TheWelcome />
  </main>

  <button @click="increment">Count is: {{ count }}</button>
  <button @click="triggerError">Trigger Error</button>
  <button :disabled="isButtonDisabled">Boolean Attributes Button</button>
  <div v-bind="objectOfAttrs">Dynamically Binding Multiple Attributes</div>
  <div :style="'color: red;'">Argument</div>
  <div>
    <p>Dynamic argument</p>
    <a :[eventName]="getUrl()">URL</a>
  </div>
</template>

<style scoped>
header {
  line-height: 1.5;
}

.logo {
  display: block;
  margin: 0 auto 2rem;
}

button {
  margin: 10px;
  font-weight: bold;
  background-color: rgba(255, 255, 255, 0.8);
  width: 100px;
  height: 50px;
  border-radius: 10px;
  cursor: pointer;
}

@media (min-width: 1024px) {
  header {
    display: flex;
    place-items: center;
    padding-right: calc(var(--section-gap) / 2);
  }

  .logo {
    margin: 0 2rem 0 0;
  }

  header .wrapper {
    display: flex;
    place-items: flex-start;
    flex-wrap: wrap;
  }
}
</style>
