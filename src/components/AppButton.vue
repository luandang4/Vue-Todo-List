<template>
  <button
    :class="{
      'd-grid btn btn-primary me-2': true,
      'is-loading': processing
      }"
    :disabled="processing "
  >
    <slot></slot>
  </button>
</template>
<script setup>
const props = defineProps({
  type: {
    type: String,
    default: "primary"
  },
  processing: {
    type: Boolean,
    default: false
  }
});
</script>

<style scoped>
button {
  position: absolute;
  top: 50%;
  left: 50%;
}

@keyframes spinner {
  to {transform: rotate(360deg);}
}

.is-loading { color: transparent;}
 
.is-loading:before {
  content: '';
  box-sizing: border-box;
  position: absolute;
  top: 50%;
  left: 50%;
  width: 20px;
  height: 20px;
  margin-top: -10px;
  margin-left: -10px;
  border-radius: 50%;
  border: 2px solid #ccc;
  border-top-color: #000;
  animation: spinner .6s linear infinite;
}
</style>